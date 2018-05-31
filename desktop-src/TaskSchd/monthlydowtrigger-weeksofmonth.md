---
title: MonthlyDOWTrigger.WeeksOfMonth property
description: For scripting, gets or sets the weeks of the month during which the task runs.
ms.assetid: 55bbf8d6-6ff6-46a3-82e2-b5986ee3927e
keywords:
- WeeksOfMonth property Task Scheduler
- WeeksOfMonth property Task Scheduler , MonthlyDOWTrigger object
- MonthlyDOWTrigger object Task Scheduler , WeeksOfMonth property
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# MonthlyDOWTrigger.WeeksOfMonth property

For scripting, gets or sets the weeks of the month during which the task runs.

## Syntax


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## Property value

A bitwise mask that indicates the days of the week during which the task runs.

## Remarks

The following table shows the mapping of the bitwise mask used by this property.



| Week                     | Hex Value | Decimal Value |
|--------------------------|-----------|---------------|
| First week of the month  | 0X01      | 1             |
| Second week of the month | 0x02      | 2             |
| Third week of the month  | 0X04      | 4             |
| Fourth week of the month | 0X08      | 8             |



 

When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                          |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                    |
| Type library<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## See also

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Task Scheduler](task-scheduler-start-page.md)
</dt> </dl>

 

 




