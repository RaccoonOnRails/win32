---
Description: The GetPin method retrieves a pin. This method implements the pure virtual CBaseFilterGetPin method.
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: CSource.GetPin method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CSource.GetPin method

The `GetPin` method retrieves a pin. This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.

## Syntax


```C++
CBasePin* GetPin(
   int n
);
```



## Parameters

<dl> <dt>

*n* 
</dt> <dd>

Number of the specified pin.

</dd> </dl>

## Return value

Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CSource Class**](csource.md)
</dt> </dl>

 

 



