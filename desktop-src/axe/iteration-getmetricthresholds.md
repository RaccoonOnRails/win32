---
title: Iteration GetMetricThresholds method
description: Returns the MetricThresholdCollection for the Iteration.
ms.assetid: 48242467-76C2-49DF-BE5B-C3E6E1DB3FD3
keywords:
- GetMetricThresholds method Access Execution Engine
- GetMetricThresholds method Access Execution Engine , Iteration interface
- Iteration interface Access Execution Engine , GetMetricThresholds method
topic_type:
- apiref
api_name:
- Iteration.GetMetricThresholds
api_location:
- AxeCore.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Iteration::GetMetricThresholds method

Returns the [**MetricThresholdCollection**](metricthresholdcollection.md) for the **Iteration**.

## Syntax


```C++
virtual HRESULT GetMetricThresholds(
  [out] MetricThresholdCollection **metricThresholds
) = 0;
```



## Parameters

<dl> <dt>

*metricThresholds* \[out\]
</dt> <dd>

The **MetricThresholdCollection**.

</dd> </dl>

## Return value

If the function succeeds, it returns **S\_OK**. If it fails, it returns an error value.

## Remarks

The **MetricThresholdCollection** holds information from element **Iteration/MetricThresholds**.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                              |
| Minimum supported server<br/> | Windows Server 2008 R2 \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>AxeRuntime.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AxeCore.dll</dt> </dl>  |



## See also

<dl> <dt>

[**Iteration**](iteration-struct.md)
</dt> </dl>

 

 




