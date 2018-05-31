---
Description: Not implemented.
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: IXml2DexCreateGraphFromFile method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# IXml2Dex::CreateGraphFromFile method

> [!Note]  
> \[Deprecated. This API may be removed from future releases of Windows.\]

 

Not implemented.

## Syntax


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## Parameters

<dl> <dt>

*ppGraph* 
</dt> <dd>

Reserved.

</dd> <dt>

*pTimeline* 
</dt> <dd>

Reserved.

</dd> <dt>

*FileName* 
</dt> <dd>

Reserved.

</dd> </dl>

## Return value

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Remarks

> [!Note]  
> The header file Qedit.h is not compatible with Direct3D headers later than version 7.

 

> [!Note]  
> To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](http://go.microsoft.com/fwlink/p/?linkid=129787). Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.

 

## See also

<dl> <dt>

[**IXml2Dex Interface**](ixml2dex.md)
</dt> </dl>

 

 


