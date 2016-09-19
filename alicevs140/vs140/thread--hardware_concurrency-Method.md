---
title: "thread::hardware_concurrency Method"
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
ms.assetid: ef68405a-cdee-4078-9cca-2c6137fb8304
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# thread::hardware_concurrency Method
Static method that returns an estimate of the number of hardware thread contexts.  
  
## Syntax  
  
```  
static unsigned int hardware_concurrency() _NOEXCEPT;  
```  
  
## Return Value  
 An estimate of the number of hardware thread contexts. If the value cannot be computed or is not well defined, this method returns 0.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [thread Class](../vs140/thread-Class.md)   
 [<thread\>](../vs140/-thread-.md)