---
Description: The Win32\_MemoryDeviceLocation association WMI class relates a memory device and the physical memory on which it exists.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: Win32\_MemoryDeviceLocation class
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Win32\_MemoryDeviceLocation class

The **Win32\_MemoryDeviceLocation** association [WMI class](https://msdn.microsoft.com/library/aa393244) relates a memory device and the physical memory on which it exists.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties. Properties are listed in alphabetic order, not MOF order.

## Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## Members

The **Win32\_MemoryDeviceLocation** class has these types of members:

-   [Properties](#properties)

### Properties

The **Win32\_MemoryDeviceLocation** class has these properties.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Data type: **Win32\_PhysicalMemory**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](https://msdn.microsoft.com/library/aa392157), [**Override**](https://msdn.microsoft.com/library/aa393650) ("Antecedent"), [**Max**](https://msdn.microsoft.com/library/aa393650) (1), [**MappingStrings**](https://msdn.microsoft.com/library/aa393650) ("WMI\|Win32\_PhysicalMemory")
</dt> </dl>

A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Data type: **Win32\_MemoryDevice**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](https://msdn.microsoft.com/library/aa392157), [**Override**](https://msdn.microsoft.com/library/aa393650) ("Dependent"), [**MappingStrings**](https://msdn.microsoft.com/library/aa393650) ("WMI\|Win32\_MemoryDevice")
</dt> </dl>

A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.

</dd> </dl>

## Remarks

The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_Realizes**](cim-realizes.md)
</dt> <dt>

[Computer System Hardware Classes](computer-system-hardware-classes.md)
</dt> </dl>

 

 



