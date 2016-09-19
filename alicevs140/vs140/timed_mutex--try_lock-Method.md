---
title: "timed_mutex::try_lock Method"
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
ms.assetid: 4ef05eb4-ba7a-4716-b21c-894f8fbdcb55
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# timed_mutex::try_lock Method
Attempts to obtain ownership of the `mutex` without blocking.  
  
## Syntax  
  
```cpp  
bool try_lock();  
```  
  
## Return Value  
 `true` if the method successfully obtains ownership of the `mutex`; otherwise, `false`.  
  
## Remarks  
 If the calling thread already owns the `mutex`, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)   
 [timed_mutex Class](../vs140/timed_mutex-Class.md)