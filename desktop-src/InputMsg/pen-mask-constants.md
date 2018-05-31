---
title: Pen Mask
description: Values that can appear in the penMask field of the POINTER\_PEN\_INFO structure.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Pen Mask

Values that can appear in the **penMask** field of the [**POINTER\_PEN\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_pen_info?branch=master) structure.

<dl> <dt>

<span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN\_MASK\_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Default. None of the optional fields are valid.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN\_MASK\_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



**pressure** of the [**POINTER\_PEN\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_pen_info?branch=master) structure is valid.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN\_MASK\_ROTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



**rotation** of the [**POINTER\_PEN\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_pen_info?branch=master) structure is valid.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN\_MASK\_TILT\_X** 
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



**tiltX** of the [**POINTER\_PEN\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_pen_info?branch=master) structure is valid.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN\_MASK\_TILT\_Y**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



**tiltY** of the [**POINTER\_PEN\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_pen_info?branch=master) structure is valid.


</dt> </dl> </dd> </dl>

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                           |
| Minimum supported server<br/> | Windows Server 2012 \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## See also

<dl> <dt>

[Constants](constants.md)
</dt> <dt>

[**POINTER\_INFO**](/windows/win32/Winuser/ns-rimext-tagpointer_info?branch=master)
</dt> </dl>

 

 




