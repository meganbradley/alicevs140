---
title: "User (VSPerfCmd)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ee1a478e-374d-4f30-ae28-d260b9d4723a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# User (VSPerfCmd)
The **User** option specifies the domain and user name of the account that owns the profiled process. This option is required only if the process is running as a user other than the logged on user. The process owner is listed in the User Name column on the Processes tab of Windows Task Manager.  
  
 The **User** option can only be specified on a command line that also contains the **Start** option option.  
  
## Syntax  
  
```  
VSPerfCmd.exe /Start:Method /Output:FileName /User:[Domain\]UserName [Options]  
```  
  
#### Parameters  
 `Domain`  
 The name of the user's domain.  
  
 `UserName`  
 The name of the user.  
  
## Required Options  
 The **User** option can only be used with the **Start** option.  
  
 **Start:** `Method`  
 Initializes the profiler to the specified profiling method.  
  
## Example  
 The following example demonstrates the use of the **User** option.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /User:SYSTEM  
```  
  
## See Also  
 [VSPerfCmd.exe Reference](../vs140/VSPerfCmd.md)   
 [Command-Line Profiling of Stand-Alone Applications](../vs140/Command-Line-Profiling-of-Stand-Alone-Applications.md)   
 [Command-Line Profiling of ASP.NET Web Applications](../vs140/Command-Line-Profiling-of-ASP.NET-Web-Applications.md)   
 [Command-Line Profiling of Services](../vs140/Command-Line-Profiling-of-Services.md)