---
Description: The following Direct Manipulation Class GUIDs are defined in DirectManipulation.idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: Direct Manipulation GUIDs
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Direct Manipulation GUIDs

The following [Direct Manipulation](direct-manipulation-portal.md) Class GUIDs are defined in DirectManipulation.idl.

-   [Master class-IDs](#master-class-ids)
-   [Secondary content class-IDs](#secondary-content-class-ids)
-   [Behavior objects class-IDs](#behavior-objects-class-ids)
-   [Related topics](#related-topics)

## Master class-IDs



| GUID                                     | Description                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | DirectManipulationManager Class. This object provides access to all [Direct Manipulation](direct-manipulation-portal.md) features and APIs available to the application.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | DCompManipulationCompositor Class. This is an implementation of the [**IDirectManipulationCompositor**](/windows/previous-versions/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor?branch=master) that wraps DirectComposition. Through this compositor object DirectManipulation can apply the output by setting transforms directly on the DComp tree. |



 

## Secondary content class-IDs



| GUID                                  | Description                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID\_VerticalIndicatorContent**   | Vertical Panning Indicator. A visual element that shows your current position in content that extends off-screen vertically.     |
| **CLSID\_HorizontalIndicatorContent** | Horizontal Panning Indicator. A visual element that shows your current position in content that extends off-screen horizontally. |
| **CLSID\_VirtualViewportContent**     | Virtual Viewport. A virtual viewport can be used to respect fixed position elements for viewports with zoom configured.          |



 

## Behavior objects class-IDs



| GUID                                     | Description                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID\_DragDropConfigurationBehavior** | Drag & Drop Behavior. Enables items to be selected and dragged.                                                                                       |
| **CLSID\_AutoScrollBehavior**            | Autoscroll Behavior. Enables content to automatically scroll as it approaches the boundary of a given axis.                                           |
| **CLSID\_DeferContactService**           | Contact deferral behavior. The amount of time (in millliseconds) to wait before calling [**SetContact**](/windows/previous-versions/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact?branch=master). |



 

## Related topics

<dl> <dt>

[Direct Manipulation](direct-manipulation-portal.md)
</dt> <dt>

[**ActivateConfiguration**](/windows/previous-versions/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration?branch=master)
</dt> <dt>

[**AddConfiguration**](/windows/previous-versions/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration?branch=master)
</dt> <dt>

[**IDirectManipulationCompositor**](/windows/previous-versions/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor?branch=master)
</dt> </dl>

 

 


