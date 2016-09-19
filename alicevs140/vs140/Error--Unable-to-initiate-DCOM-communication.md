---
title: "Error: Unable to initiate DCOM communication"
ms.custom: na
ms.date: 09/19/2016
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
ms.assetid: 2a7b27e6-2526-4f32-bc4d-eaee447f24ec
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: Unable to initiate DCOM communication
A DCOM error occurred when the local machine tried to communicate with the remote machine. This is caused by a firewall on the remote server or broken Windows authentication on the remote machine.  
  
### To correct this error  
  
-   If the remote machine has Windows Firewall enabled, see [How to: Set Up Remote Debugging](../vs140/Set-Up-the-Remote-Tools-on-the-Device.md) for instructions about how to configure the firewall for local debugging.  
  
-   To restore Windows authentication, try rebooting both machines. Examine event logs on local and remote machines for Kerberos errors and contact domain administrators for known problems.  
  
## See Also  
 [Remote Debugging Setup](../vs140/Remote-Debugging.md)