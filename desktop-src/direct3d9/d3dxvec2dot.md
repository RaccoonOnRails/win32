---
Description: Determines the dot product of two 2D vectors.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: D3DXVec2Dot function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# D3DXVec2Dot function

Determines the dot product of two 2D vectors.

## Syntax


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## Parameters

<dl> <dt>

*pV1* \[in\]
</dt> <dd>

Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***

Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.

</dd> <dt>

*pV2* \[in\]
</dt> <dd>

Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***

Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.

</dd> </dl>

## Return value

Type: **[**FLOAT**](winprog.windows_data_types)**

The dot product.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Math Functions](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2CCW**](d3dxvec2ccw.md)
</dt> </dl>

 

 



