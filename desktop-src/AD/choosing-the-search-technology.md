---
title: Choosing the Search Technology
description: This topic includes a list of technologies used to search Active Directory.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.prod: windows-server-dev
ms.technology: active-directory-domain-services
ms.tgt_platform: multiple
keywords:
- search technologies in Active Directory Active Directory
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Choosing the Search Technology

The technologies, listed in the following table, can be used to search in Active Directory Domain Services.



| Technology                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](http://go.microsoft.com/fwlink/p/?linkid=83869)<br/> | The [DirectorySearcher](http://go.microsoft.com/fwlink/p/?linkid=83869) class is provided by the [System.DirectoryServices](http://go.microsoft.com/fwlink/p/?linkid=83863) namespace to allow searching within Active Directory Domain Services with .NET Framework. For more information, see [Searching the Directory](http://go.microsoft.com/fwlink/p/?linkid=83967).<br/>                                                                                                                                  |
| [**IDirectorySearch**](https://msdn.microsoft.com/library/aa746362)<br/>                       | ADSI provides the [**IDirectorySearch**](https://msdn.microsoft.com/library/aa746362) interface to query an Active Directory server, as well as other directory services such as NDS, using LDAP. **IDirectorySearch** is a COM interface that returns richly typed data, such as Integer, Octet String, String, Security Descriptor, UTC-Time, Large Integer, or Boolean. For more information about how to use **IDirectorySearch**, see [Searching With the IDirectorySearch Interface](https://msdn.microsoft.com/library/aa746472).<br/> |
| OLE DB<br/>                                                              | OLE DB is a set of COM interfaces that provide applications with uniform access to data stored in diverse data sources, regardless of location or type. ADSI also provides an OLE DB provider for ADSI that enables applications to use OLE DB to access Active Directory Domain Services. The ADSI OLE DB provider uses the [**IDirectorySearch**](https://msdn.microsoft.com/library/aa746362) interfaces to submit queries to Active Directory Domain Services and to collect the results.<br/>                                     |
| ADO and other OLE DB-based data access technologies<br/>                 | The ADSI OLE DB provider enables any data-access technology based on OLE DB, such as ADO, to search within Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| LDAP API<br/>                                                            | Windows 2000 domain controllers are directory servers that are compliant with LDAP version 3. The LDAP API is a C-style function library. Applications can use the LDAP API to search within Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                              |



 

Consider the following when choosing a technology:

-   For Microsoft Visual Basic and Visual Basic Scripting Edition (VBScript), ADO is recommended.
-   For C/C++, you can choose any of the technologies.
-   If your application extensively uses ADSI, it may be simpler to use [**IDirectorySearch**](https://msdn.microsoft.com/library/aa746362). If you use [**IDirectoryObject**](https://msdn.microsoft.com/library/aa746355) to manage objects in Active Directory Domain Services, use **IDirectorySearch** to make handling the properties returned from the search easier. **IDirectorySearch** uses the same [**ADSVALUE**](https://msdn.microsoft.com/library/aa772241) structures as **IDirectoryObject** to represent properties. In addition, **IDirectorySearch** is exposed on almost all ADSI COM objects. If you have a pointer to an ADSI COM object, you can call **QueryInterface** to get an **IDirectorySearch** pointer that you can use to perform a search starting at the directory object represented by the ADSI COM object.
-   If your application already uses OLE DB, ADO, or LDAP API, you can continue to use those technologies to search within Active Directory Domain Services.
-   If your application must join data from an Active Directory Domain Service and a SQL Server 7 database, use OLE DB. By using OLE DB, your application can perform distributed queries that reference Active Directory Domain Services and tables and rowsets from one or more Microsoft SQL Server 7 databases.

 

 




