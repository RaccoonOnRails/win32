---
title: RequestTimeout
description: RequestTimeout
ms.assetid: 18c2b223-2105-4d8d-aef9-157d19a80f92
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# RequestTimeout

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/library/windows/desktop/aa965362) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.

 

The **RequestTimeout** entry is the amount of time a query client should wait before it returns a failure to connect to a named pipe instance in Indexing Service.

### Summary



|          |                    |
|----------|--------------------|
| Type:    | **REG\_DWORD**     |
| Units:   | Milliseconds       |
| Default: | 10000 (10 seconds) |
| Range:   | 0 - 1000000000     |



 

### Remarks

If Indexing Service is not running, the client immediately returns a failure to connect.

The value of an identically named entry under the [**Catalog**](catalog--property--and-scope-registry-entries.md) subkey for a specific catalog cannot override the value of this entry.

## Related topics

<dl> <dt>

[Main Registry Entries](main-registry-entries.md)
</dt> </dl>

 

 



