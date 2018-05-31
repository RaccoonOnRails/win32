---
Description: Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: CBasePinm\_bTryMyTypesFirst member
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CBasePin::m\_bTryMyTypesFirst member

Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.

## Syntax


```C++
bool m_bTryMyTypesFirst;
```



## Remarks

This flag defaults to **FALSE**. If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBasePin Class**](cbasepin.md)
</dt> </dl>

 

 



