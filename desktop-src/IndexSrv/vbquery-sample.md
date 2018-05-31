---
title: VBQuery Sample
description: VBQuery Sample
ms.assetid: a4666588-3ab2-4ed3-9a5b-bd536a63c051
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# VBQuery Sample

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/library/windows/desktop/aa965362) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.

 

The VBQuery sample is an example Windows application written in Visual Basic that illustrates how to query Indexing Service using the Indexing Service query languages and the [ActiveX Data Objects (ADO)](programming-apis.md#-idxs-activex-data-objects-api) and [Query Helper](programming-apis.md#-idxs-query-helper-api) APIs.

Source: mssdk\\samples\\winbase\\indexing\\VBQuery\\

**To build and run the sample**

1.  In the Visual Basic development environment, open the VBQuery.vbp project in the source path of the sample.
2.  In the **File** menu, select **Make VBQuery.exe**.
3.  In the **Make Project** dialog box, click **OK**.
4.  In the **Run** menu, click **Start**.

**To execute queries using the sample**

1.  Make sure that Indexing Service is started.
2.  In the **Query** text box, enter the query text.
3.  In the **Scope** text box, enter the folder where you want to start the search. You can click the "..." button to display a dialog box to find a folder for the scope of the search.
4.  In the **Sort** list, select the way you want the application to sort the search hits.
5.  In the list next to the **Sort** list, select the Indexing Service query language used to specify the query.
6.  Click **Go** to run the specified query or **Clear** to specify a new query.

## Programming Notes

The VBQuery sample illustrates how you can use the [Query](iixssoquery.md) and [Utility](iixssoutil.md) automation objects of the Query Helper API to build applications that query a catalog. The sample can process queries specified in any of the following three query languages.

-   [Indexing Service Query Language](indexing-service-query-language.md), Dialect 1 or Dialect 2
-   [SQL Query Language](sql-query-language.md)

In addition, the sample uses ADO objects to handle the recordsets returned by the Query Helper Automation objects.

This sample also demonstrates making a dynamic-link library (DLL) call to the [LocateCatalogs](/windows/win32/Ntquery/nf-ntquery-locatecatalogsa?branch=master) function of the [OLE DB Helper API](programming-apis.md#-idxs-ole-db-helper-api). The application uses this function to locate catalogs suitable for the scope specified by the user.

 

 



