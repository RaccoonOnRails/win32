---
Description: Forces the Enhanced Video Renderer (EVR) to use bob deinterlacing.
ms.assetid: 56f808b3-c2eb-46e4-84a1-c478a5db78e7
title: EVRConfig\_ForceBob attribute
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# EVRConfig\_ForceBob attribute

Forces the Enhanced Video Renderer (EVR) to use bob deinterlacing.

## Data type

**UINT32**

## Get/set

To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/mfobjects/nf-mfobjects-imfattributes-getuint32?branch=master).

To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/mfobjects/nf-mfobjects-imfattributes-setuint32?branch=master).

## Remarks

This attribute can be set on the EVR media sink. To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/win32/mfobjects/nn-mfobjects-imfattributes?branch=master) interface.

Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_ForceBob** flag on the EVR. See [**MFVideoMixPrefs**](/windows/win32/evr/ne-evr-_mfvideomixprefs?branch=master) for a description of this flag.

The GUID constant for this attribute is exported from strmiids.lib.

## Requirements



|                                     |                                                                                    |
|-------------------------------------|------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                         |
| Minimum supported server<br/> | Windows Server 2008 R2 \[desktop apps only\]<br/>                            |
| Header<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## See also

<dl> <dt>

[Alphabetical List of Media Foundation Attributes](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR Attributes](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Video Quality Management](video-quality-management.md)
</dt> </dl>

 

 



