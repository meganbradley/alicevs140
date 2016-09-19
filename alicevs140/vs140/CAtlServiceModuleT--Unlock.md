---
title: "CAtlServiceModuleT::Unlock"
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
ms.assetid: e76cbc84-78a7-47aa-a846-08473deab0bc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::Unlock
Decrements the service's lock count.  
  
## Syntax  
  
```  
  
LONG Unlock( ) throw( );  
  
```  
  
## Return Value  
 Returns the lock count, which may be useful for diagnostics and debugging.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)