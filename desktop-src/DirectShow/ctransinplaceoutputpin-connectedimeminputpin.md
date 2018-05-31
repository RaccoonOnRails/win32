---
Description: The ConnectedIMemInputPin method retrieves a pointer to the downstream input pin. This method returns the CBaseOutputPinm\_pInputPin member variable.
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: CTransInPlaceOutputPin.ConnectedIMemInputPin method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CTransInPlaceOutputPin.ConnectedIMemInputPin method

The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin. This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.

## Syntax


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## Parameters

This method has no parameters.

## Return value

Returns a pointer to the [**IMemInputPin**](/windows/win32/Strmif/nn-strmif-imeminputpin?branch=master) interface on the downstream input pin.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CTransInPlaceOutputPin Class**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 



