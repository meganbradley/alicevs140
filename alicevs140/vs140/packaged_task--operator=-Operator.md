---
title: "packaged_task::operator= Operator"
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
ms.assetid: bf0f6948-5c68-4921-87eb-cff9d5aa1c82
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# packaged_task::operator= Operator
Transfers the *associated asynchronous state* from a specified object.  
  
## Syntax  
  
```cpp  
packaged_task& operator=(packaged_task&& Right);  
```  
  
#### Parameters  
 `Right`  
 A `packaged_task` object.  
  
## Return Value  
 `*this`  
  
## Remarks  
 After the operation, `Right` no longer has an associated asynchronous state.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [packaged_task Class](../vs140/packaged_task-Class.md)   
 [<future\>](../vs140/-future-.md)