---
title: Displaying XML Output from WinRM Scripts
description: Windows Remote Management scripts return XML rather than objects. The XML is not in a human-readable format. You can use the methods of the MSXML API and the preinstalled XSL file to transform the data into human-readable format.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.prod: windows-server-dev
ms.technology: windows-remote-management
ms.tgt_platform: multiple
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Displaying XML Output from WinRM Scripts

Windows Remote Management scripts return XML rather than objects. The XML is not in a human-readable format. You can use the methods of the [MSXML](http://go.microsoft.com/fwlink/p/?linkid=57523) API and the preinstalled XSL file to transform the data into human-readable format.

For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).

The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form. If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.

**To format raw XML output**

1.  Create the [**WSMan**](wsman.md) object and create a session.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Create MSXML objects that represent the XML response output and the XSL transform.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Obtain data through [**Session**](session.md) object methods.

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Supply the response to the MSXML [loadXML](http://go.microsoft.com/fwlink/p/?linkid=84374) method and the [load](http://go.microsoft.com/fwlink/p/?linkid=84377) method to store the transform file.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Use the MSXML [transformNode](http://go.microsoft.com/fwlink/p/?linkid=84376) method and display or save the output.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

The following VBScript code example shows the complete script.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## Adding a Portable Subroutine to Transform XML to Your Scripts

You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.

The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



The following subroutine transforms each line of your data as shown in the following example.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("http://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub 
```



## Related topics

<dl> <dt>

[About Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Using Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[Windows Remote Management Reference](windows-remote-management-reference.md)
</dt> </dl>

 

 



