---
Description: Converts the specified mesh subset into a single triangle strip.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: D3DXConvertMeshSubsetToSingleStrip function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# D3DXConvertMeshSubsetToSingleStrip function

Converts the specified mesh subset into a single triangle strip.

## Syntax


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## Parameters

<dl> <dt>

*MeshIn* \[in\]
</dt> <dd>

Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**

Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.

</dd> <dt>

*AttribId* \[in\]
</dt> <dd>

Type: **[**DWORD**](winprog.windows_data_types)**

Attribute ID of the mesh subset to convert to strips.

</dd> <dt>

*IBOptions* \[in\]
</dt> <dd>

Type: **[**DWORD**](winprog.windows_data_types)**

Combination of one or more flags from the [**D3DXMESH**](direct3d9.d3dxmesh) enumeration, specifying options for creating the index buffer. Cannot be D3DXMESH\_32BIT. The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.

</dd> <dt>

*ppIndexBuffer* \[out\]
</dt> <dd>

Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/d3d9helper/nn-d3d9-idirect3dindexbuffer9?branch=master)\***

Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/d3d9helper/nn-d3d9-idirect3dindexbuffer9?branch=master) interface, representing the index buffer containing the strip.

</dd> <dt>

*pNumIndices* \[out\]
</dt> <dd>

Type: **[**DWORD**](winprog.windows_data_types)\***

Number of indices in the buffer returned in the *ppIndexBuffer* parameter.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.

## Remarks

Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Mesh Functions](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 



