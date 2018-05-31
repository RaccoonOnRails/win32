---
Description: Sent to a window when the size or position of the window is about to change. An application can use this message to override the windows default maximized size and position, or its default minimum or maximum tracking size.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: WM\_GETMINMAXINFO message
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# WM\_GETMINMAXINFO message

Sent to a window when the size or position of the window is about to change. An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.

A window receives this message through its [**WindowProc**](/windows/win32/Winuser/nf-winuser-callwindowproca?branch=master) function.


```C++
#define WM_GETMINMAXINFO                0x0024
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

This parameter is not used.

</dd> <dt>

*lParam* 
</dt> <dd>

A pointer to a [**MINMAXINFO**](/windows/win32/Winuser/ns-winuser-tagminmaxinfo?branch=master) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes. An application can override the defaults by setting the members of this structure.

</dd> </dl>

## Return value

Type: **LRESULT**

If an application processes this message, it should return zero.

## Remarks

The maximum tracking size is the largest window size that can be produced by using the borders to size the window. The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

**Reference**
</dt> <dt>

[**MoveWindow**](/windows/win32/Winuser/nf-winuser-movewindow?branch=master)
</dt> <dt>

[**SetWindowPos**](/windows/win32/Winuser/nf-winuser-setwindowpos?branch=master)
</dt> <dt>

[**MINMAXINFO**](/windows/win32/Winuser/ns-winuser-tagminmaxinfo?branch=master)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 



