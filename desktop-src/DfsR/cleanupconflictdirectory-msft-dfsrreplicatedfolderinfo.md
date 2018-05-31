---
title: CleanupConflictDirectory method of the MSFT\_DfsrReplicatedFolderInfo class
description: Starts the Conflict and Deleted folder cleanup process.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: f7ff9ea3-955e-4f24-99ad-f261e3ecc916
ms.prod: windows-server-dev
ms.technology:
- distributed-file-system-replication
- windows-management-instrumentation
ms.tgt_platform: multiple
keywords:
- CleanupConflictDirectory method Distributed File System Replication
- CleanupConflictDirectory method Distributed File System Replication , MSFT_DfsrReplicatedFolderInfo class
- MSFT_DfsrReplicatedFolderInfo class Distributed File System Replication , CleanupConflictDirectory method
topic_type:
- apiref
api_name:
- MSFT_DfsrReplicatedFolderInfo.CleanupConflictDirectory
api_location:
- DfsRWmiV2.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# CleanupConflictDirectory method of the MSFT\_DfsrReplicatedFolderInfo class

Starts the Conflict and Deleted folder cleanup process.

## Syntax


```mof
uint32 CleanupConflictDirectory();
```



## Parameters

This method has no parameters.

## Return value

This method returns one of the [MONITOR\_STATUS return codes](monitor-status-return-codes.md) or one of the [system error codes](https://msdn.microsoft.com/library/windows/desktop/ms681381).

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2012 R2<br/>                                                        |
| Namespace<br/>                | Root\\Microsoft\\Windows\\Dfsr<br/>                                                |
| MOF<br/>                      | <dl> <dt>Dfsrwmiv2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DfsRWmiV2.dll</dt> </dl> |



## See also

<dl> <dt>

[**MSFT\_DfsrReplicatedFolderInfo**](msft-dfsrreplicatedfolderinfo.md)
</dt> </dl>

 

 




