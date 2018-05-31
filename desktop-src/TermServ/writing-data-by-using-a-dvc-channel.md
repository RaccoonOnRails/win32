---
title: Writing Data by Using a DVC Channel
description: Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.prod: windows-server-dev
ms.technology: remote-desktop-services
ms.tgt_platform: multiple
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Writing Data by Using a DVC Channel

Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client. The writing of channel data is implemented by the [**Write**](/windows/win32/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write?branch=master) method of the [**IWTSVirtualChannel**](/windows/win32/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel?branch=master) interface.

The following illustration shows the sending and receiving of the data packet between the DVC client and server (DVC plug-in).

![sending and receiving a data packet between the dvc client and server](images/writedvcchannel.png)

 

 



