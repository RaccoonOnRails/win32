---
title: VML EndArrow Attribute
description: VML EndArrow Attribute
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# VML EndArrow Attribute

This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9. Webpages and applications that rely on VML should be [migrated to SVG](http://go.microsoft.com/fwlink/p/?LinkID=236964) or other widely supported standards.

> [!Note]  
> As of December 2011, this topic has been archived. As a result, it is no longer actively maintained. For more information, see [Archived Content](https://msdn.microsoft.com/library/hh772377). For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](http://go.microsoft.com/fwlink/p/?linkid=204313).

 

Defines an arrowhead for the end of a line. Read/write. **String**.

**Applies To**

[Stroke](msdn-online-vml-stroke-element.md)

**Tag Syntax**

&lt;v: *element* endarrow=" *expression* "&gt;

**Script Syntax**

*element* .endarrow="*expression*"

*expression*=*element*.endarrow

**Remarks**

Values include:

-   None (default)
-   Block
-   Classic
-   Diamond
-   Oval
-   Open

*VML Standard Attribute*

**Example**

A line is drawn with a classic arrowhead on the end of the stroke.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 



