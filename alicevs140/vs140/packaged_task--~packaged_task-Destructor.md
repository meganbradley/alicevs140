---
title: "packaged_task::~packaged_task Destructor"
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
ms.assetid: 4ef4e98f-af9e-469e-a077-afecef0e59e8
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# packaged_task::~packaged_task Destructor
Destroys a `packaged_task` object.  
  
## Syntax  
  
```cpp  
~packaged_task();  
```  
  
## Remarks  
 If the *associated asynchronous state* is not *ready*, the destructor stores a [future_error](../vs140/future_error-Class.md) exception that has an error code of `broken_promise` as the result in the associated asynchronous state, and any threads that are blocked on the associated asynchronous state become unblocked.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [packaged_task Class](../vs140/packaged_task-Class.md)   
 [<future\>](../vs140/-future-.md)