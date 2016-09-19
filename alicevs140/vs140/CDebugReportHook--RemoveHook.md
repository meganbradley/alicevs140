---
title: "CDebugReportHook::RemoveHook"
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
ms.assetid: 0cff2557-f154-4525-b87d-8a61bcf7bd74
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDebugReportHook::RemoveHook
Call this method to stop sending debug reports to the named pipe and restore the previous report hook.  
  
## Syntax  
  
```  
  
void RemoveHook( ) throw( );  
  
```  
  
## Remarks  
 Calls [_CrtSetReportHook2](../vs140/_CrtSetReportHook2--_CrtSetReportHookW2.md) to restore the previous report hook.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CDebugReportHook Class](../vs140/CDebugReportHook-Class.md)   
 [CDebugReportHook::SetHook](../vs140/CDebugReportHook--SetHook.md)