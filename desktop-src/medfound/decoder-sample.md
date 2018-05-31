---
Description: Shows how to write a decoder for Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Decoder Sample
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Decoder Sample

Shows how to write a decoder for Microsoft Media Foundation.

This sample implements a mock MPEG-1 video decoder that displays the time code for each video frame. It does not actually decode the MPEG-1 bitstream. The following image shows the video output from the decoder.

![screen shot of a video frame from the decoder](images/decodersample.png)

> [!Note]  
> Prior to the Windows SDK for Windows 7, this sample was included as part of the [MPEG1Source Sample](mpeg1source-sample.md).

 

## APIs Demonstrated

This sample demonstrates the following Media Foundation interfaces:

-   [**IMFTransform**](/windows/win32/mftransform/nn-mftransform-imftransform?branch=master)

## Requirements



| Product                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](http://go.microsoft.com/fwlink/p/?linkid=129787) | Windows 7 |



 

## Downloading the Sample

This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).

## Related topics

<dl> <dt>

[Media Foundation SDK Samples](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation Transforms](media-foundation-transforms.md)
</dt> <dt>

[Writing a Custom MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 


