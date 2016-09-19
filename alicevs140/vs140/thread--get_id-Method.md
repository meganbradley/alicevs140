---
title: "thread::get_id Method"
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
ms.assetid: 5780f829-589a-4e80-b0fb-b8bff29777c1
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# thread::get_id Method
Returns a unique identifier for the associated thread.  
  
## Syntax  
  
```  
id get_id() const _NOEXCEPT;  
```  
  
## Return Value  
 A [thread::id](../vs140/thread--id-Class.md) object that uniquely identifies the associated thread, or `thread::id()` if no thread is associated with the object.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [thread Class](../vs140/thread-Class.md)   
 [<thread\>](../vs140/-thread-.md)