---
Description: The GetBorderColour method retrieves the current window border color, m\_BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: CBaseControlWindow.GetBorderColour method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CBaseControlWindow.GetBorderColour method

The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.

## Syntax


```C++
COLORREF GetBorderColour();
```



## Parameters

This method has no parameters.

## Return value

Returns the color of the border.

## Remarks

An application can set a destination rectangle to display the video. This rectangle should be relative to the client area for the window. If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border. The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function. This property affects the color of the border. Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/win32/Control/nf-control-ivideowindow-get_bordercolor?branch=master) method.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseControlWindow Class**](cbasecontrolwindow.md)
</dt> </dl>

 

 



