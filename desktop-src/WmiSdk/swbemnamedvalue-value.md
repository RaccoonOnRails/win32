---
Description: The Value property of the SWbemNamedValue object returns the variant value of an SWbemNamedValue item.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.prod: windows-server-dev
ms.technology: windows-management-instrumentation
ms.tgt_platform: multiple
title: SWbemNamedValue.Value property
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# SWbemNamedValue.Value property

The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item. This is the default property for **SWbemNamedValue** objects. Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.

For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

This property is read/write.

## Syntax


```VB
SWbemNamedValue.Value As Variant
```



## Property value

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Type library<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID\_SWbemNamedValue<br/>                                                       |
| IID<br/>                      | IID\_ISWbemNamedValue<br/>                                                        |



 

 



