---
title: "CDebugReportHook::CDebugReportHook"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: c08bbebc-2254-405e-adbf-2184fdcdeac7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDebugReportHook::CDebugReportHook
Calls [SetPipeName](../vs140/CDebugReportHook--SetPipeName.md), [SetTimeout](../vs140/CDebugReportHook--SetTimeout.md), and [SetHook](../vs140/CDebugReportHook--SetHook.md).  
  
## Syntax  
  
```  
  
      CDebugReportHook(  
   LPCSTR szMachineName = ".",  
   LPCSTR szPipeName = "AtlsDbgPipe",  
   DWORD dwTimeout = 20000  
) throw();  
```  
  
#### Parameters  
 `szMachineName`  
 The name of the machine to which the debug output should be sent. Defaults to the local machine.  
  
 `szPipeName`  
 The name of the named pipe to which the debug output should be sent.  
  
 `dwTimeout`  
 The time in milliseconds that this class will wait for the named pipe to become available.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CDebugReportHook Class](../vs140/CDebugReportHook-Class.md)