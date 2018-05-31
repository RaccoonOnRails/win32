---
Description: The advanced security property sheet enables the user to perform editing operations that are not available on the basic security property page of an access control editor.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Advanced Security Property Sheet
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Advanced Security Property Sheet

The advanced security property sheet enables the user to perform editing operations that are not available on the [basic security property page](basic-security-property-page.md) of an access control editor. The property sheet can include the following property pages:

-   A [Permissions](permissions-property-page.md) property page for advanced editing of the object's [*discretionary access control list*](https://msdn.microsoft.com/library/windows/desktop/ms721573#-security-discretionary-access-control-list-gly) (DACL), such as editing [object-specific ACEs](object-specific-aces.md) or controlling [ACE inheritance](ace-inheritance.md).
-   An [Auditing](auditing-property-page.md) property page for viewing and editing the object's [*system access control list*](https://msdn.microsoft.com/library/windows/desktop/ms721625#-security-system-access-control-list-gly) (SACL).
-   An [Owner](owner-property-page.md) property page for changing the object's owner.

The user can display the advanced security property sheet by clicking the **Advanced** button on the basic security property page. To display the **Advanced** button, set the SI\_ADVANCED flag in the [**SI\_OBJECT\_INFO**](/windows/win32/Aclui/ns-aclui-_si_object_info?branch=master) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/Aclui/?branch=master) implementation.

 

 


