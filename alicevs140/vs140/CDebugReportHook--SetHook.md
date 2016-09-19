---
title: "CDebugReportHook::SetHook"
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
ms.assetid: 8a13d625-ba7f-43b3-944d-e9cc9feecaae
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDebugReportHook::SetHook
Call this method to start sending debug reports to the named pipe.  
  
## Syntax  
  
```  
  
void SetHook( ) throw( );  
  
```  
  
## Remarks  
 Calls [_CrtSetReportHook2](../vs140/_CrtSetReportHook2--_CrtSetReportHookW2.md) to have debug reports routed through [CDebugReportHookProc](../vs140/CDebugReportHook--CDebugReportHookProc.md) to the named pipe. This class keeps track of the previous report hook so that it can be restored when [RemoveHook](../vs140/CDebugReportHook--RemoveHook.md) is called.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CDebugReportHook Class](../vs140/CDebugReportHook-Class.md)