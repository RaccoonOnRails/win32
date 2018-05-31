---
title: Shared Connections
description: Using the ICS API, you can determine whether a particular connection can be shared. Not all connections can be shared.
ms.assetid: cbae930a-97d1-4fec-8063-5fc1cdfcdb4e
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Shared Connections

\[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the [Windows Firewall API](windows-firewall-start-page.md).\]

A connection is considered to be either public or private.

A public connection connects a local computer with the public Internet. A public connection is often through a modem, broadband connection (DSL or cable), or T1 line.

A private connection connects a local computer with other computers on a home or office local area network (LAN). Private connections are typically through network interface cards (NICs) but could also be through an IEEE 1394 ("Firewire") connection, serial cable, or some form of wireless device.

When ICS is enabled, one public and at least one private connection must be specified. Multiple private connections can be specified and are automatically bridged together to form one segment. It is only possible to share one public connection at a time.

When enabled, ICS receives packets on private connections, translates them via NAT, and routes them to the Internet through the public connection.

Using the ICS API, you can determine whether a particular connection can be shared. Not all connections can be shared.

Before attempting to configure sharing on a connection use the [**INetSharingManager::get\_NetConnectionProps**](/windows/previous-versions/NetCon/nf-netcon-inetsharingmanager-get_netconnectionprops?branch=master) method to obtain an [**INetConnectionProps**](/windows/previous-versions/NetCon/nn-netcon-inetconnectionprops?branch=master) interface for the connection. Then, use the [**INetConnectionProps::get\_MediaType**](/windows/previous-versions/NetCon/nf-netcon-inetconnectionprops-get_mediatype?branch=master) method to obtain the media type for the connection. If the **NETCON\_MEDIATYPE** for the connection is one of the following:

-   NCM\_PHONE
-   NCM\_DIRECT
-   NCM\_ISDN
-   NCM\_LAN
-   NCM\_TUNNEL
-   NCM\_PPPOE

Use the [**INetConnection::GetProperties**](/windows/previous-versions/NetCon/nf-netcon-inetconnection-getproperties?branch=master) method to check the [**NETCON\_CHARACTERISTIC\_FLAGS**](/windows/previous-versions/NetCon/ne-netcon-tagnetcon_characteristic_flags?branch=master) for the connection. If the NCCF\_INCOMING\_ONLY flag is absent, the connection is sharable.

To configure sharing on a particular connection, use the [**INetSharingManager::get\_INetSharingConfigurationForINetConnection**](/windows/previous-versions/NetCon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection?branch=master) method to obtain an [**INetSharingConfiguration**](/windows/previous-versions/NetCon/nn-netcon-inetsharingconfiguration?branch=master) interface for the connection.

 

 



