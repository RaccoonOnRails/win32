---
Description: D3D10\_RECT is declared as follows
ms.assetid: a0b27fb0-1e48-4e46-ad8c-99f197c31dc2
title: D3D10\_RECT
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# D3D10\_RECT

D3D10\_RECT is declared as follows:

``` syntax
typedef RECT D3D10_RECT;
```

For more information about this GDI rectangle structure, see [RECT](http://msdn2.microsoft.com/en-us/library/ms536136.aspx).

## Remarks

This structure is used for scissor rectangles by [**ID3D10Device::RSGetScissorRects**](/windows/win32/D3D10/nf-d3d10-id3d10device-rsgetscissorrects?branch=master) and [**ID3D10Device::RSSetScissorRects**](/windows/win32/D3D10/nf-d3d10-id3d10device-rssetscissorrects?branch=master).

## Requirements



|                    |                                                                                      |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3D10.h</dt> </dl>   |
| Library<br/> | <dl> <dt>D3D10.lib</dt> </dl> |



## See also

<dl> <dt>

[Core Structures](d3d10-graphics-reference-d3d10-core-structures.md)
</dt> </dl>

 

 



