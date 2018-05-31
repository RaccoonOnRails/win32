---
Description: The DiscountRateEnd property is a value that indicates the time at which the discount period for transmitting faxes ends. The discount period applies to outgoing faxes.
ms.assetid: 6fd58501-eddd-4634-8023-5a3266e7eade
title: FaxOutgoingQueue.DiscountRateEnd property
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FaxOutgoingQueue.DiscountRateEnd property

The **DiscountRateEnd** property is a value that indicates the time at which the discount period for transmitting faxes ends. The discount period applies to outgoing faxes.

This property is read/write.

## Syntax


```VB
Property DiscountRateEnd As Date
```



## Property value

A **Date** that specifies or receives the hour and minute, expressed in local system time, when the discount period for transmitting faxes ends.

## Remarks

To read or to write to this property, a user must have the [****farQUERY\_CONFIG****](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master) access right.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>FaxComex.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Fxscomex.dll</dt> </dl> |



## See also

<dl> <dt>

[**FaxOutgoingQueue**](-mfax-faxoutgoingqueue.md)
</dt> <dt>

[**IFaxOutgoingQueue**](/windows/previous-versions/FaxComex/nn-faxcomex-ifaxoutgoingqueue?branch=master)
</dt> <dt>

[Setting the Outgoing Queue Properties](-mfax-setting-the-outgoing-queue-properties.md)
</dt> </dl>

 

 



