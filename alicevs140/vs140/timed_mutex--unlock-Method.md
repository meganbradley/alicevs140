---
title: "timed_mutex::unlock Method"
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
ms.assetid: a243399b-8107-4b57-8acf-a254c7be1fa1
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# timed_mutex::unlock Method
Releases ownership of the `mutex`.  
  
## Syntax  
  
```cpp  
void unlock();  
```  
  
## Remarks  
 If the calling thread does not own the `mutex`, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)   
 [timed_mutex Class](../vs140/timed_mutex-Class.md)