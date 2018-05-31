---
Description: Enables or disables speaker fill in an audio decoder or digital signal processor (DSP).
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: AVDSPSpeakerFill property
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# AVDSPSpeakerFill property

Enables or disables speaker fill in an audio decoder or digital signal processor (DSP).

This property is read/write.

## Data type

**UINT32** (**VT\_UI4**)

## Property GUID

**CODECAPI\_AVDSPSpeakerFill**

## Property value

The value of this property is a member of the [**eAVDSPSpeakerFill**](/windows/win32/codecapi/ne-codecapi-eavdspspeakerfill?branch=master) enumeration.

## Remarks

Speaker fill is a DSP process that converts mono or stereo audio into multichannel audio.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps \| UWP apps\]<br/>                     |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps \| UWP apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## See also

<dl> <dt>

[Codec API Properties](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/win32/Strmif/nn-strmif-icodecapi?branch=master)
</dt> </dl>

 

 



