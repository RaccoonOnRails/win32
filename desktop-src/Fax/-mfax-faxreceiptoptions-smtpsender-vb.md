---
Description: The SMTPSender property is a null-terminated string that contains the Simple Mail Transport Protocol (SMTP) email address for the sender of the mail message receipt.
ms.assetid: e25fa002-a47b-438e-965a-ada0bd861e17
title: FaxReceiptOptions.SMTPSender property
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FaxReceiptOptions.SMTPSender property

The **SMTPSender** property is a null-terminated string that contains the Simple Mail Transport Protocol (SMTP) email address for the sender of the mail message receipt.

This property is read/write.

## Syntax


```VB
Property SMTPSender As String
```



## Property value

A **String** that specifies or receives the SMTP email address for the sender of the fax. The string is a null-terminated.

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

[**FaxReceiptOptions**](-mfax-faxreceiptoptions.md)
</dt> <dt>

[**IFaxReceiptOptions**](/windows/previous-versions/FaxComex/nn-faxcomex-ifaxreceiptoptions?branch=master)
</dt> <dt>

[Setting Receipt Options](-mfax-setting-receipt-options.md)
</dt> </dl>

 

 



