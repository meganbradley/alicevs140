---
title: "Error: Firewall No Authentication"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dda1acb8-bed7-4bc8-9991-9cdc49c2ac1e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: Firewall No Authentication
The Internet Connection Firewall on the remote machine is not set up to allow remote debugging. For remote debugging with `No Authentication`, msvsmon.exe must be added to the exceptions list. Opening some IPSEC ports may be necessary as well.  
  
> [!NOTE]
>  The remote debugger is able to automatically configure the Windows Firewall. When using a firewall other than the Windows Firewall such as third party software firewall or a hardware firewall, the firewall must be manually configured to allow remote debugging. To do so, allow traffic on TCP/IP ports that msvsmon.exe is listening on. By default, these are port 4018 and 4019, where 4018 is used on all Operating Systems, and 4019 is used only on Windows x64 to allow debugging x86 processes.  
  
 For more information, see [How to: Set Up Remote Debugging](../vs140/Set-Up-the-Remote-Tools-on-the-Device.md).