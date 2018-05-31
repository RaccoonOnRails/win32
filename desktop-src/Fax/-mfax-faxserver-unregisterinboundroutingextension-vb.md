---
Description: The UnregisterInboundRoutingExtension method unregisters an existing inbound routing extension. Unregistration will take place only after the fax server is restarted.
ms.assetid: 982e5a78-d37a-4156-8882-2f8ab4d1d04a
title: FaxServer.UnregisterInboundRoutingExtension method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FaxServer.UnregisterInboundRoutingExtension method

The **UnregisterInboundRoutingExtension** method unregisters an existing inbound routing extension. Unregistration will take place only after the fax server is restarted.

## Syntax


```VB
FaxServer.UnregisterInboundRoutingExtension( _
  ByVal bstrExtensionName As String _
) As Long
```



## Parameters

<dl> <dt>

*bstrExtensionName* 
</dt> <dd>

Type: **String**

String value that specifies the internal name of the fax routing extension DLL.

</dd> </dl>

## Remarks

Only an administrator can unregister a routing extension. Also, this method works only on the local fax server.

To use this method, a user must have the [**farMANAGE\_CONFIG**](/windows/previous-versions/FaxComex/ne-faxcomex-fax_access_rights_enum?branch=master) access right.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>FaxComex.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Fxscomex.dll</dt> </dl> |



## See also

<dl> <dt>

[**FaxServer**](-mfax-faxserver.md)
</dt> <dt>

[**IFaxServer**](/windows/previous-versions/FaxComex/nn-faxcomex-ifaxserver?branch=master)
</dt> </dl>

 

 



