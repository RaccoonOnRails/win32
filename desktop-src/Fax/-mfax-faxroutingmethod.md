---
Description: The FaxRoutingMethod object permits a fax client application to access fax routing configuration information for a fax port on a connected fax server.
ms.assetid: d759d840-80a4-4e59-a8e6-1cc6adc399ce
title: FaxRoutingMethod
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# FaxRoutingMethod

The FaxRoutingMethod object permits a fax client application to access fax routing configuration information for a fax port on a connected fax server. Use this object to retrieve and set routing information for a specific fax port and to enable or disable a fax routing method on a port.

A FaxRoutingMethod object is created by a [FaxRoutingMethods](-mfax-faxroutingmethods.md) object.

A fax client application must create an instance of a [FaxServer](-mfax-faxserver-client.md) object before accessing most other objects that begin with Fax. (A fax server connection is not required to access a [FaxTiff](-mfax-faxtiff.md) object.)

## C/C++

-   Create by calling the [**IFaxRoutingMethods::get\_Item**](/windows/previous-versions/Faxcom/nf-faxcom-ifaxroutingmethods-get_item?branch=master) method.
-   Supports the [**IFaxRoutingMethod**](/windows/previous-versions/Faxcom/nn-faxcom-ifaxroutingmethod?branch=master) interface.

For more information about creating an instance of a FaxRoutingMethod object, and for a list of the object's properties and methods, see [**IFaxRoutingMethod**](/windows/previous-versions/Faxcom/nn-faxcom-ifaxroutingmethod?branch=master).

## Visual Basic

Create by retrieving the [**Item**](-mfax-faxroutingmethods-object-visual-basic-.md) property of the [**FaxRoutingMethods**](-mfax-faxroutingmethods-object-visual-basic-.md) object.

For more information about creating a FaxRoutingMethod object, and for a list of the properties and methods of the object, see [**FaxRoutingMethod object (Visual Basic)**](-mfax-faxroutingmethod-object-visual-basic-.md).

 

 


