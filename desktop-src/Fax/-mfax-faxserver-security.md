---
Description: The Security property creates a FaxSecurity configuration object. The object permits the calling application to set and retrieve a security descriptor for the fax server.
ms.assetid: 67ddcb57-d00f-4145-8ce0-0532411b1fd2
title: FaxServer.Security property
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FaxServer.Security property

The **Security** property creates a [**FaxSecurity**](-mfax-faxsecurity.md) configuration object. The object permits the calling application to set and retrieve a security descriptor for the fax server.

This property is read-only.

## Syntax


```VB
Property Security As FaxSecurity
```



## Property value

A [**FaxSecurity**](-mfax-faxsecurity.md) object.

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

 

 



