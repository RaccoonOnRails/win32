---
Description: The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a Win32\_PerfRawData instance.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.prod: windows-server-dev
ms.technology: windows-management-instrumentation
ms.tgt_platform: multiple
title: COOKER\_VARIANCE
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# COOKER\_VARIANCE

The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a [**Win32\_PerfRawData**](https://msdn.microsoft.com/library/aa394299) instance. The variance is calculated by dividing the sum of the square of the deviation from the mean of each counter by the number of counters. In other words, the variance is the average of the squared deviations from the mean for each counter. This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](https://msdn.microsoft.com/library/windows/desktop/aa373083).

For more information about the counter type formula, see [Counter Types](http://go.microsoft.com/fwlink/p/?linkid=44341).

For more information about high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).

## Example Code

For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).

## Related topics

<dl> <dt>

[Statistical Counter Types](statistical-counter-types.md)
</dt> <dt>

[Monitoring Performance Data](monitoring-performance-data.md)
</dt> </dl>

 

 


