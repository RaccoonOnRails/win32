---
title: MultipleResponseInteractions Complex Type
description: Defines a collection of interactions that let the user select more than one choice from a list of choices.
ms.assetid: b9fd9d2c-2ef8-41bb-a474-49302845e78d
keywords:
- MultipleResponseInteractions complex type Windows Troubleshooting Toolkit
topic_type:
- apiref
api_name:
- MultipleResponseInteractions
api_type:
- Schema
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# MultipleResponseInteractions Complex Type

Defines a collection of interactions that let the user select more than one choice from a list of choices.

``` syntax
<xs:complexType name="MultipleResponseInteractions">
    <xs:sequence>
        <xs:element name="MultipleResponseInteraction"
            type="dcmPS:MultipleResponseInteraction"
            minOccurs="1"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## Child elements



| Element                     | Type                                                                                         | Description                                                                                                   |
|-----------------------------|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| MultipleResponseInteraction | [**dcmPS:MultipleResponseInteraction**](package-multipleresponseinteraction-complextype.md) | A collection of interactions that let the user select more than one choice from a list of choices.<br/> |



## Requirements



|                                     |                                                         |
|-------------------------------------|---------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>              |
| Minimum supported server<br/> | Windows Server 2008 R2 \[desktop apps only\]<br/> |



## See also

<dl> <dt>

[**Interactions Complex Type**](package-interactions-complextype.md)
</dt> <dt>

[**MultipleResponseInteractions (Interactions) Element**](package-multipleresponseinteractions-interactions-element.md)
</dt> </dl>

 

 




