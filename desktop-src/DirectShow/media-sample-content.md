---
Description: Describes the contents of an elementary stream within an MPEG-2 transport stream. This enumeration is used in the IMPEG2PIDMap interface, which is implemented on the output pins of the MPEG-2 Demultiplexer.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: MEDIA\_SAMPLE\_CONTENT enumeration
ms.date: 05/31/2018
ms.topic: enumeration
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# MEDIA\_SAMPLE\_CONTENT enumeration

Describes the contents of an elementary stream within an MPEG-2 transport stream. This enumeration is used in the [**IMPEG2PIDMap**](/windows/win32/Bdaiface/nn-bdaiface-impeg2pidmap?branch=master) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).

## Syntax


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## Constants

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**
</dt> <dd>

Specifies a complete transport stream packet to be passed through without processing.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**
</dt> <dd>

Specifies an audio or video PES payload.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**
</dt> <dd>

Specifies a PAT, PMT, CAT, or Private data stream. These are complete PSI sections which do not need to be reassembled.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**
</dt> <dd>

Specifies gathered TS packet payloads, such as PES packets.

</dd> </dl>

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Bdatypes.h (include Bdaiface.h)</dt> </dl> |



## See also

<dl> <dt>

[DirectShow Enumerated Types](directshow-enumerated-types.md)
</dt> </dl>

 

 



