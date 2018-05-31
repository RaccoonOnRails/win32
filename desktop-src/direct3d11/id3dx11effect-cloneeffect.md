---
title: ID3DX11Effect CloneEffect method
description: Creates a copy of an effect interface.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- CloneEffect method Direct3D 11
- CloneEffect method Direct3D 11 , ID3DX11Effect interface
- ID3DX11Effect interface Direct3D 11 , CloneEffect method
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ID3DX11Effect::CloneEffect method

Creates a copy of an effect interface.

## Syntax


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## Parameters

<dl> <dt>

*Flags* 
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

Flags affecting the creation of the cloned effect. Can be 0 or one of the following values.



| Flag                                    | Description                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE | Ignore all "single" qualifiers on cbuffers. All cbuffers will have their own [**ID3D11Buffer**](/windows/win32/D3D11/nn-d3d11-id3d11buffer?branch=master)s created in the cloned effect. |



 

</dd> <dt>

*ppClonedEffect* 
</dt> <dd>

Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***

Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).

## Remarks

> [!Note]  
> The DirectX SDK does not supply any compiled binaries for effects. You must use Effects 11 source to build your effects-type application. For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## Requirements



|                    |                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Library<br/> | <dl> <dt>N/A (An Effects 11 library is available online as shared source.)</dt> </dl> |



## See also

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 




