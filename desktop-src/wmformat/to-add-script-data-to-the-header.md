---
title: To Add Script Data to the Header
description: To Add Script Data to the Header
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK,adding script data to headers
- Advanced Systems Format (ASF),adding script data to headers
- ASF (Advanced Systems Format),adding script data to headers
- scripts,adding data to headers
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# To Add Script Data to the Header

You can include script commands in the header of an ASF file. To write script commands to the header at the time of encoding, perform the following steps. Perform these steps prior to calling [**IWMWriter::BeginWriting**](/windows/win32/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting?branch=master).

1.  Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.
2.  Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/windows/win32/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript?branch=master). Each call takes the two strings separately and the presentation time to be used for the command as parameters.

When an application reads the file, it will need to retrieve all of the script commands. To find all script commands in the header of a file, perform the following steps. This should be done before starting playback.

1.  Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.
2.  Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/windows/win32/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount?branch=master).
3.  Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/windows/win32/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript?branch=master).
4.  Create a list of the presentation times so that your application can react to the commands at the appropriate time.

> [!Note]  
> When using DRM to encrypt a file, no script command can have a presentation time of 0.

 

## Related topics

<dl> <dt>

[**IWMHeaderInfo Interface**](/windows/win32/wmsdkidl/nn-wmsdkidl-iwmheaderinfo?branch=master)
</dt> <dt>

[**IWMWriter Interface**](/windows/win32/wmsdkidl/nn-wmsdkidl-iwmwriter?branch=master)
</dt> <dt>

[**Using Script Commands**](using-script-commands.md)
</dt> </dl>

 

 



