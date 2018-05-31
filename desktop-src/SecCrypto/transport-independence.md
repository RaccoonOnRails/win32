---
Description: Certificates can be requested and distributed through any transport mechanism.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Transport Independence
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Transport Independence

Certificates can be requested and distributed through any transport mechanism. Certificate Services accepts [*certificate requests*](security.c_gly#-security-certificate-request-gly) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport. Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.

Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++. The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.

 

 


