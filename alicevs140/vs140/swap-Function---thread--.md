---
title: "swap Function (&lt;thread&gt;)"
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
ms.topic: article
ms.assetid: 5db784d4-e334-450d-9e3c-4c121b2a14dc
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap Function (&lt;thread&gt;)
Swaps the states of two `thread` objects.  
  
## Syntax  
  
```  
void swap(  
   thread& Left,  
   thread& Right  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Left`  
 The left `thread` object.  
  
 `Right`  
 The right `thread` object.  
  
## Remarks  
 The function calls `Left.swap(Right)`.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [thread Class](../vs140/thread-Class.md)   
 [<thread\>](../vs140/-thread-.md)   
 [thread::swap Method](../vs140/thread--swap-Method.md)