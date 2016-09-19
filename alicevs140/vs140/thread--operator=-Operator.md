---
title: "thread::operator= Operator"
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
ms.assetid: 7b69dca5-b979-449a-bff0-ef427820e948
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# thread::operator= Operator
Associates the thread of a specified object with the current object.  
  
## Syntax  
  
```  
thread& operator=(  
   thread&& Other  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Other`  
 A `thread` object.  
  
## Return Value  
 `*this`  
  
## Remarks  
 The method calls detach if the calling object is joinable.  
  
 After the association is made, `Other` is set to a default-constructed state.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [thread Class](../vs140/thread-Class.md)   
 [<thread\>](../vs140/-thread-.md)