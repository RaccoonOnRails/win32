---
Description: Not implemented and cannot be used.
ms.assetid: b41ba894-5cee-458d-935f-e89363925968
title: SslChangeNotify function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# SslChangeNotify function

The **SslChangeNotify** function is not implemented and cannot be used.

## Syntax


```C++
SECURITY_STATUS WINAPI SslChangeNotify(
  _In_ HANDLE hEvent,
  _In_ DWORD  dwFlags
);
```



## Parameters

<dl> <dt>

*hEvent* \[in\]
</dt> <dd>

This parameter is reserved for future use.

</dd> <dt>

*dwFlags* \[in\]
</dt> <dd>

This parameter is reserved for future use.

</dd> </dl>

## Return value

Returns **NTE\_NOT\_SUPPORTED**.

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                           |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 



