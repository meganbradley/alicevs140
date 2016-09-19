---
title: "Error: The Microsoft Visual Studio Remote Debugging Monitor on the remote computer does not have permission to connect to this computer"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
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
ms.assetid: ba08a59b-6dbc-4bbc-9c52-379d3bf5241f
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: The Microsoft Visual Studio Remote Debugging Monitor on the remote computer does not have permission to connect to this computer
This error occurs when the user who is trying to run the Visual Studio Remote Debugging Monitor (msvsmon) does not have an account on the local computer.  
  
### To fix this problem  
  
-   Add a user account to the Visual Studio debugger host computer, with the same name and password as the user account running msvsmon on the remote computer,  
  
     \- or -  
  
-   Run msvsmon as a user who has permission to call into the local computer. This means the user must be a domain user and an administrator on the msvsmon computer. You can specify the user account to run msvsmon in one of two ways:  
  
    -   Right-click the msvsmon icon and choose **Run As** on the shortcut menu  
  
     \- or -  
  
    -   At the Command Prompt, run `runas.exe`.  
  
## See Also  
 [Remote Debugging Across Domains](../vs140/Remote-Debugging-Across-Domains.md)   
 [Remote Debugging Errors and Troubleshooting](../vs140/Remote-Debugging-Errors-and-Troubleshooting.md)   
 [Remote Debugging](../vs140/Remote-Debugging.md)