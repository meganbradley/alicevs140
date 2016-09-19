---
title: "CDebugReportHook::SetPipeName"
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
ms.assetid: eee1c2f7-49ad-4d70-ad73-3155cecc945e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDebugReportHook::SetPipeName
Call this method to set the machine and name of the pipe to which the debug reports will be sent.  
  
## Syntax  
  
```  
  
      BOOL SetPipeName(  
   LPCSTR szMachineName = ".",  
   LPCSTR szPipeName = "AtlsDbgPipe"   
) throw( );  
```  
  
#### Parameters  
 `szMachineName`  
 The name of the machine to which the debug output should be sent.  
  
 `szPipeName`  
 The name of the named pipe to which the debug output should be sent.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CDebugReportHook Class](../vs140/CDebugReportHook-Class.md)