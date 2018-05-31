---
Description: Allows the callback to modify the CFM\_XXX values passed to IContextMenuQueryContextMenu.
title: DFM\_MODIFYQCMFLAGS message
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# DFM\_MODIFYQCMFLAGS message

Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/win32/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu?branch=master).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## Parameters

<dl> <dt>

*puNewFlags* \[in\]
</dt> <dd>

A pointer to the new flag values.

</dd> <dt>

*uFlags* \[in\]
</dt> <dd>

Flags that specify how the context menu can be changed. This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/win32/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu?branch=master).

</dd> </dl>

## Requirements



|                                     |                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                          |
| Minimum supported server<br/> | Windows Server 2008 R2 \[desktop apps only\]<br/>                             |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 



