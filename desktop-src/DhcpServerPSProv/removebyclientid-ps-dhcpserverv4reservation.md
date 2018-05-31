---
title: RemoveByClientId method of the PS\_DhcpServerv4Reservation class
description: Deletes the IPv4 Reservation from the specified scope.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 6cc0393e-6794-4a8a-b419-35fc6e4a5ff5
ms.prod: windows-server-dev
ms.technology:
- dhcp-server
- windows-management-instrumentation
ms.tgt_platform: multiple
keywords:
- RemoveByClientId method
- RemoveByClientId method, PS_DhcpServerv4Reservation class
- PS_DhcpServerv4Reservation class, RemoveByClientId method
topic_type:
- apiref
api_name:
- PS_DhcpServerv4Reservation.RemoveByClientId
api_location:
- DhcpServerPsProvider.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# RemoveByClientId method of the PS\_DhcpServerv4Reservation class

Deletes the IPv4 Reservation from the specified scope.

## Syntax


```mof
uint32 RemoveByClientId(
  [in]  string                  ScopeId,
  [in]  string                  ClientId[],
  [in]  string                  ComputerName,
  [in]  boolean                 PassThru,
  [out] DhcpServerv4Reservation cmdletOutput[]
);
```



## Parameters

<dl> <dt>

*ScopeId* \[in\]
</dt> <dd>

Scope identifier (in IPv4 address format) from which the reservations are to be deleted

</dd> <dt>

*ClientId* \[in\]
</dt> <dd>

Client identifier(s) of the reservations which are to be deleted. For Windows clients, MAC address is used as a client identifier.

</dd> <dt>

*ComputerName* \[in\]
</dt> <dd>

DNS name or IP address of the target computer running the DHCP server service.

</dd> <dt>

*PassThru* \[in\]
</dt> <dd>

If this parameter is specified, the cmdlet returns the PowerShell object which is modified.

</dd> <dt>

*cmdletOutput* \[out\]
</dt> <dd>

An embedded instance of the [**DhcpServerv4Reservation**](dhcpserverv4reservation.md) class.

</dd> </dl>

## Requirements



|                                     |                                                                                                     |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                           |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                                      |
| Namespace<br/>                | Root\\Microsoft\\Windows\\DHCP<br/>                                                           |
| MOF<br/>                      | <dl> <dt>DhcpServerPsProvider.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DhcpServerPsProvider.dll</dt> </dl> |



## See also

<dl> <dt>

[**PS\_DhcpServerv4Reservation**](ps-dhcpserverv4reservation.md)
</dt> </dl>

 

 




