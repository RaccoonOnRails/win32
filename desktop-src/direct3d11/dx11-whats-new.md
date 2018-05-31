---
title: Whats New in the August 2009 Windows 7/Direct3D 11 SDK
description: This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# What's New in the August 2009 Windows 7/Direct3D 11 SDK

This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text. The Direct2D API is designed to interoperate well with Direct3D and GDI. This SDK allows developers to evaluate the API and write simple applications, with some of the more advanced functionality possible on properly configured machines. <br/> [Documentation](http://go.microsoft.com/fwlink/p/?linkid=141057) and [samples](http://go.microsoft.com/fwlink/p/?linkid=141058) for Direct2D are currently available on MSDN.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite provides support for high-quality text rendering, resolution-independent outline fonts, full Unicode text and layout support, and much, much more:<br/>
<ul>
<li>A device-independent text layout system that improves text readability in documents and in UI.<br/></li>
<li>High-quality, sub-pixel, ClearType text rendering that can use GDI Direct3D, Direct2D, or application-specific rendering technology.<br/></li>
<li>Support for multi-format text. <br/></li>
<li>Support for the advanced typography features of OpenType fonts.<br/></li>
<li>Support for the layout and rendering of text in all languages supported by Windows.<br/></li>
</ul>
This SDK allows developers to evaluate the API and write basic applications for demonstration purposes only.<br/> [Documentation](http://go.microsoft.com/fwlink/p/?linkid=141059) and [samples](http://go.microsoft.com/fwlink/p/?linkid=141060) for DirectWrite are currently available on MSDN.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1<br/></td>
<td>[DXGI 1.1](https://msdn.microsoft.com/library/windows/desktop/bb219822) builds on DXGI 1.0 and will be available on both Windows Vista and Windows 7. DXGI 1.1 adds several new features:<br/>
<ul>
<li>Synchronized Shared Surfaces Support. This enables efficient read and write surface sharing between multiple D3D (could be between D3D10 and D3D11) devices.<br/></li>
<li>BGRA format support. This allows GDI to render to the same DXGI surface targeted by a Direct2D, Direct3D 10.1 or Direct3D 11 device. <br/></li>
<li>Maximum Frame Latency. Using [<strong>IDXGIDevice1::SetMaximumFrameLatency</strong>](https://msdn.microsoft.com/library/windows/desktop/ff471334) and [<strong>IDXGIDevice1::GetMaximumFrameLatency</strong>](https://msdn.microsoft.com/library/windows/desktop/ff471332), titles can control the number of frames that are allowed to be stored in a queue, before submission for rendering. Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.<br/></li>
<li>Adapter Enumeration. Using [<strong>IDXGIFactory1::EnumAdapters1</strong>](https://msdn.microsoft.com/library/windows/desktop/ff471336), titles can enumerates local adapters without any monitors or outputs attached, as well as adapters with outputs attached.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Updated Samples<br/></td>
<td>This release has several new and updated samples.<br/>
<ul>
<li>The new [AdaptiveTessellationCS40](7cb17765-22d8-42fe-68ec-104a8db543e5) is an illustration of more advanced compute shader processing techniques that can be run on a D3D10 or D3D11 GPU.</li>
<li>The [HDRToneMappingCS11 sample](d325cd30-56e1-d608-6ab6-2755caf2b1b1) has been expanded to implement blur and bloom effects (in addition to tone mapping) using compute shader, as well as providing pixel shader implementations for comparison.</li>
<li>The [MultithreadedRendering11 sample](089de2b0-a2d6-3c99-6ff6-684a1ab3d4de) has been significantly updated, with more complex art assets and more intensive per-thread processing.</li>
<li>The [SubD11 sample](5608dcd2-0114-5056-d87c-d2f7f775ea14) has been updated with a new facial model, and the sample now leverages the adjacency computation feature of the Samples Content Exporter.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## Related topics

<dl> <dt>

[Features Introduced In Previous Releases](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

 

 




