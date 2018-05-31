---
Description: Signals that a media stream does not have data available at a specified time.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: MEStreamTick event
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# MEStreamTick event

Signals that a media stream does not have data available at a specified time.

## Event values

Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/win32/mfobjects/nf-mfobjects-imfmediaevent-getvalue?branch=master) include the following.



| VARTYPE           | Description                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT\_I8<br/> | Time at which the gap occurs, in 100-nanosecond units.<br/> <br/> |



## Remarks

This event signals a gap in the data. The event notifies downstream components not to expect any data at the specified time.

The event should be sent by whichever object generates the time stamps for the media samples in the stream. Depending on the format of the data, this is either:

-   The media stream on the media source ([**IMFMediaStream**](/windows/win32/mfidl/nn-mfidl-imfmediastream?branch=master) interface), or
-   The decoder transform ([**IMFTransform**](/windows/win32/mftransform/nn-mftransform-imftransform?branch=master) interface).

During the gap, the object should send the event about as often as it would normally produce samples. For video, send one event for each missing frame. For audio, send the event at least once per second during the gap. The value of the event is the time stamp of the missing sample. Send as many MEStreamTick events as needed to fill the gap in the data.

If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events. For example, if there is a gap in both audio and video data, then both streams send the event.

The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/win32/mfidl/nf-mfidl-imfmediastream-requestsample?branch=master) request. The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.

Media sinks cannot consume this event directly. To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/win32/mfidl/nf-mfidl-imfstreamsink-placemarker?branch=master) with an **MFSTREAMSINK\_MARKER\_TICK** marker. The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.

Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event. The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.

> [!Note]  
> An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.

 

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                                           |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Events](media-foundation-events.md)
</dt> </dl>

 

 



