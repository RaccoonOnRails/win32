---
Description: For converting media files into ASF format, you can use Windows Media encoders. To use these encoders, they must be registered with the system.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Creating an Encoder by Using CoCreateInstance
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Creating an Encoder by Using CoCreateInstance

For converting media files into ASF format, you can use Windows Media encoders. To use these encoders, they must be registered with the system. Encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs) and must expose the IMFTransform interface. This topic describes how an application can get a pointer to the required MFT encoder's IMFTransform interface and instantiate it for use.

For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).

-   [Using an Encoder's IMFTransform Interface](#creating-an-encoder-by-using-cocreateinstance)
    -   [Encoder Creation Example](#encoder-creation-example)
-   [Related topics](#related-topics)

## Using an Encoder's IMFTransform Interface

Upon successful registration of Windows Media encoders with the system, an application can enumerate the encoders by calling [**MFTEnum**](/windows/win32/mfapi/nf-mfapi-mftenum?branch=master). To search for the right encoder, you must specify the following:

-   The GUID that represents the category, which is either **MFT\_CATEGORY\_AUDIO\_ENCODER** or **MFT\_CATEGORY\_VIDEO\_ENCODER**.

-   The format to match. This is set in the [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/mfobjects/ns-mfobjects-__midl___midl_itf_mfobjects_0000_0008_0003?branch=master) structure that specifies the major type and subtype of the media type that the encoder will generate samples in. This structure is passed in the *pOutputType* parameter. For information about the supported types, see [Media Type GUIDs](media-type-guids.md).

    > [!Note]  
    > The input type information in the *pInputType* parameter is not required. This is because the input type is known to the application and the encoder expects the input stream to be in an uncompressed format.

     

[**MFTEnum**](/windows/win32/mfapi/nf-mfapi-mftenum?branch=master) returns an array of [**IMFTransform**](/windows/win32/mftransform/nn-mftransform-imftransform?branch=master) pointers for the encoder MFTs that match the search criteria. You can instantiate an encoder by calling the COM function **CoCreateInstance** and passing the CLSID of the encoder you want to use. This function returns a pointer to the **IMFTransform** interface that represents the encoder. For more information about this function call, see the Windows SDK documentation for the Component Object Model (COM).

### Encoder Creation Example

The following code example shows how to create an audio or video encoder.


```C++
HRESULT FindEncoder(
    const GUID&amp; subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &amp;info,      // Output type
        NULL,       // Reserved
        &amp;ppCLSIDs,
        &amp;count
        );

    if (SUCCEEDED(hr) &amp;&amp; count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## Related topics

<dl> <dt>

[Instantiating an Encoder MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoders](windows-media-encoders.md)
</dt> </dl>

 

 


