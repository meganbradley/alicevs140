---
title: "Error: Firewall on Local Machine"
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
ms.assetid: ab60dda9-7934-4891-aa2f-001380d2ed83
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: Firewall on Local Machine
The Internet Connection Firewall on the local machine, the machine you are running Visual Studio from, is not set up to allow remote debugging. For managed or native remote debugging with the default transport, the TCP 135 port must be opened for DCOM traffic. File and printer sharing must be opened, and devenv.exe must be added to the exceptions list. Opening some IPSEC ports may be necessary as well.  
  
 For more information, see [How to: Set Up Remote Debugging](../vs140/Set-Up-the-Remote-Tools-on-the-Device.md).