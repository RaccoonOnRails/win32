---
title: Creating a Device Description
description: A UPnP-based device description is an XML document that describes the properties of a device and the hierarchy of nested devices within it.
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Creating a Device Description

A UPnP-based [*device description*](d-gly.md) is an XML document that describes the properties of a device and the hierarchy of nested devices within it. The schema for UPnP-based device descriptions, known as the UPnP Template Language (UTL) for devices, is defined in the UPnP device architecture. Device descriptions contain links to [*service descriptions*](s-gly.md). The schema for service descriptions and the UTL for services are also defined in the "UPnP Device Architecture" specification.

> [!Note]  
> There might be problems when using the service description from www.upnp.org.

 

The developer of a device must provide device and service descriptions for the device.

The elements of a device description that the developer of a hosted device must provide are the same as those defined in the "UPnP Device Architecture" specification, with the following exceptions:

-   The **controlURL** and **eventSubURL** elements are required and must be empty. The device host fills in values for these fields when the device is published and announced.
-   The **UDN** element must contain an identifier that is unique to the device description document (that is, it need not be globally unique). This identifier is used to look up the UDN generated by the device host.
-   The **SCPDURL** elements must not contain URLs to service descriptions. Instead, they must contain the name of the service description file. The service description file must be located in the [*resource directory*](r-gly.md). The location of this directory must be provided to the device host during the registration process, such as using a Setup program. This path and all below it are relative paths, based on the registered path.
-   The **url** element within the **icon** element must not contain URLs to device icons. Instead, they must contain the name of the icon file. If present, the icon file must be located in the resource directory. This path and all below it are relative paths, based on the registered path.
-   The **URLBase** element must not be present.

> [!Note]  
> All URLs generated by the device host are relative URLs. The URLs are relative to the location of the device description document, which is sent in the initial device announcement.

 

> \[!Important\]  
> Do not add comments to your device description document as it may cause registration failures when the Universal Plug and Play Device Host attempts to parse the document.

 

## String Length Limitations

The following string lengths are used in the Device Host API with UPnP technology:

-   **deviceType** – 64 bytes
-   **friendlyName** – 64 bytes
-   **manufacturer** – 64 bytes
-   **modelDescription** – 128 bytes
-   **modelName** – 32 bytes
-   **modelNumber** – 32 bytes
-   **serialNumber** – 64 bytes
-   **UPC** – 12 bytes
-   **serviceType** – 64 bytes
-   **serviceId** – 64 bytes

 

 



