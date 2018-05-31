---
Description: The Win32\_ClassicCOMClassSettings association WMI class relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: Win32\_ClassicCOMClassSettings class
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Win32\_ClassicCOMClassSettings class

The **Win32\_ClassicCOMClassSettings** association [WMI class](https://msdn.microsoft.com/library/aa393244) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties. Properties are listed in alphabetic order, not MOF order.

## Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## Members

The **Win32\_ClassicCOMClassSettings** class has these types of members:

-   [Properties](#properties)

### Properties

The **Win32\_ClassicCOMClassSettings** class has these properties.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Data type: **Win32\_ClassicCOMClass**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157), [**Override**](https://msdn.microsoft.com/library/aa393650) ("Element"), [**MappingStrings**](https://msdn.microsoft.com/library/aa393650) ("WMI\|Win32\_ClassicCOMClass")
</dt> </dl>

A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.

</dd> <dt>

**Setting**
</dt> <dd> <dl> <dt>

Data type: **Win32\_ClassicCOMClassSetting**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157), [**Override**](https://msdn.microsoft.com/library/aa393650) ("Setting"), [**MappingStrings**](https://msdn.microsoft.com/library/aa393650) ("WMI\|Win32\_ClassicCOMClassSetting")
</dt> </dl>

A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.

</dd> </dl>

## Remarks

The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).

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

[**CIM\_ElementSetting**](cim-elementsetting.md)
</dt> <dt>

[Operating System Classes](https://msdn.microsoft.com/library/aa392727)
</dt> </dl>

 

 



