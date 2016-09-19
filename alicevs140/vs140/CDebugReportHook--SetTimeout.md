---
title: "CDebugReportHook::SetTimeout"
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
ms.assetid: c787e1e1-0479-4f12-b54f-578a10585b9f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDebugReportHook::SetTimeout
Call this method to set the time in milliseconds that this class will wait for the named pipe to become available.  
  
## Syntax  
  
```  
  
      void SetTimeout(  
   DWORD dwTimeout   
);  
```  
  
#### Parameters  
 `dwTimeout`  
 The time in milliseconds that this class will wait for the named pipe to become available.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CDebugReportHook Class](../vs140/CDebugReportHook-Class.md)