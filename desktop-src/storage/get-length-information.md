---
title: GET\_LENGTH\_INFORMATION structure
description: The GET\_LENGTH\_INFORMATION structure is used with the IOCTL\_DISK\_GET\_LENGTH\_INFO to obtain the length, in bytes, of a disk, partition, or volume.
ms.assetid: 1c5af24f-fd99-4a64-afd4-aaa8168b1dc5
keywords:
- GET_LENGTH_INFORMATION structure Storage Devices
- PGET_LENGTH_INFORMATION structure pointer Storage Devices
topic_type:
- apiref
api_name:
- GET_LENGTH_INFORMATION
api_location:
- ntdddisk.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: structure
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# GET\_LENGTH\_INFORMATION structure

The GET\_LENGTH\_INFORMATION structure is used with the [**IOCTL\_DISK\_GET\_LENGTH\_INFO**](ioctl-disk-get-length-info.md) to obtain the length, in bytes, of a disk, partition, or volume.

## Syntax


```C++
typedef struct _GET_LENGTH_INFORMATION {
  LARGE_INTEGER Length;
} GET_LENGTH_INFORMATION, *PGET_LENGTH_INFORMATION;
```



## Members

<dl> <dt>

**Length**
</dt> <dd>

Contains the length, in bytes, of a disk, partition, or volume.

</dd> </dl>

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ntdddisk.h (include Ntdddisk.h)</dt> </dl> |



## See also

<dl> <dt>

[**IOCTL\_DISK\_GET\_LENGTH\_INFO**](ioctl-disk-get-length-info.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20GET_LENGTH_INFORMATION%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





