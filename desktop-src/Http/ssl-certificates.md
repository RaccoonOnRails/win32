---
title: SSL Certificates
description: Secure Sockets Layer (SSL) has become a standard for securing Internet connections and is used to prevent eavesdropping on the network. The SSL protocol allows a client and server to authenticate each other and negotiate encryption algorithms.
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# SSL Certificates

Secure Sockets Layer (SSL) has become a standard for securing Internet connections and is used to prevent eavesdropping on the network. The SSL protocol allows a client and server to authenticate each other and negotiate encryption algorithms.

SSL uses an encryption key and an encryption algorithm to secure the HTTP connection. The encryption keys are contained in SSL certificates used by both the client and the server. The certificate is typically an X.509 ([RFC 2459](Http://go.microsoft.com/fwlink/p/?linkid=84042)) document. The server provides the SSL certificate for the session and sends the certificate to the client in the handshake phase. The client sends its certificate to the server only if the server sends a request to the client for a certificate. Thus the client always authenticates the server but the server has the option whether or not to authenticate the client.

Server certificates must be stored in the HTTP Server API's local persistent storage, for use each time a secure connection is created. Each certificate store entry also contains the IP Address and port of the server, the certificate hash (used for signing the messages) and the application ID. The application ID is used to identify the application that owns the certificate.

System administrators can store SSL server certificate information with the configuration APIs. An administrative tool calls the [**HttpSetServiceConfiguration**](/windows/win32/Http/nf-http-httpsetserviceconfiguration?branch=master) function and specifies HttpServiceConfigSSLCertInfo value for the service configuration parameter to set information for an SSL certificate. Only one server certificate can be configured for each IP Address and port pair on the machine. The HTTP Server API also provides [**query**](/windows/win32/Http/nf-http-httpqueryserviceconfiguration?branch=master) and [**delete**](/windows/win32/Http/nf-http-httpdeleteserviceconfiguration?branch=master) functions to access or delete existing certificates.

 

 



