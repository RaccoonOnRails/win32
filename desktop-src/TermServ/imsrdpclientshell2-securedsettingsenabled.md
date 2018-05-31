---
title: IMsRdpClientShell2 SecuredSettingsEnabled property
description: Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.prod: windows-server-dev
ms.technology: remote-desktop-services
ms.tgt_platform: multiple
keywords:
- SecuredSettingsEnabled property Remote Desktop Services
- SecuredSettingsEnabled property Remote Desktop Services , IMsRdpClientShell2 interface
- IMsRdpClientShell2 interface Remote Desktop Services , SecuredSettingsEnabled property
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# IMsRdpClientShell2::SecuredSettingsEnabled property

Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.

This property is read-only.

## Syntax


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## Property value

A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.

## Requirements



|                                     |                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7<br/>                                                                          |
| Minimum supported server<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## See also

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

 




