---
title: Create New Accessible Objects
description: Create New Accessible Objects
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Create New Accessible Objects

In this scenario, the server creates a new accessible object in response to each [**OBJID\_CLIENT**](object-identifiers.md#objid-client) request.

In the following example code, a pointer to the control is retrieved from the extra window data. This and the window handle are passed to the constructor of the custom accessibility server (AccServer) object. This object is created whenever [**OBJID\_CLIENT**](object-identifiers.md#objid-client) is received.

When the object is created, the server obtains a reference, which must be released after calling [**LresultFromObject**](/windows/win32/Oleacc/nf-oleacc-lresultfromobject?branch=master), so that the object is destroyed as soon as the client is finished with it. Note that **LresultFromObject** increments the reference count several times, but it is the responsibility of client applications, and the Microsoft Active Accessibility runtime, to release these references.


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 



