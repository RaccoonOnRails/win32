---
Description: Requests a Media Foundation transform (MFT) to that streaming is about to end.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT\_MESSAGE\_NOTIFY\_END\_STREAMING
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# MFT\_MESSAGE\_NOTIFY\_END\_STREAMING

Requests a Media Foundation transform (MFT) to that streaming is about to end.

## Message Parameter

None.

## Remarks

To send this message, call [**IMFTransform::ProcessMessage**](/windows/win32/mftransform/nf-mftransform-imftransform-processmessage?branch=master).

The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.

### Implementation

The MFT can respond to this message by releasing buffers and other resources. The MFT does not flush input data or reset the media types in response to this message. An MFT is not required to respond to this message.

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                           |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## See also

<dl> <dt>

[**MFT\_MESSAGE\_TYPE**](/windows/win32/mftransform/ne-mftransform-_mft_message_type?branch=master)
</dt> </dl>

 

 



