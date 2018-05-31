---
Description: The SCE\_ENUMERATION\_CONTEXT data type is an opaque handle provided by the Security Configuration tool set. It is used by the PFSCE\_QUERY\_INFO function to navigate through the security database.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE\_ENUMERATION\_CONTEXT
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# SCE\_ENUMERATION\_CONTEXT

The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set. It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/Scesvc/nc-scesvc-pfsce_query_info?branch=master) function to navigate through the security database.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## Requirements



|                                     |                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                         |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                |
| Header<br/>                   | <dl> <dt>Scesvc.h</dt> </dl> |



## See also

<dl> <dt>

[**PFSCE\_QUERY\_INFO**](/windows/win32/Scesvc/nc-scesvc-pfsce_query_info?branch=master)
</dt> </dl>

 

 



