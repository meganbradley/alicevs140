---
title: "CAtlModule::Unlock"
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
ms.assetid: 2769ecca-7eb6-4fb8-8586-68dafe95317f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlModule::Unlock
Decrements the lock count.  
  
## Syntax  
  
```  
  
virtual LONG Unlock( ) throw( );  
  
```  
  
## Return Value  
 Decrements the lock count and returns the updated value. This value may be useful for diagnostics and debugging.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlModule Class](../vs140/CAtlModule-Class.md)