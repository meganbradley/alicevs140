---
title: "condition_variable::native_handle Method"
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
ms.assetid: ba7101b3-8e8c-408d-a897-4caba9a31fed
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# condition_variable::native_handle Method
Returns the implementation-specific type that represents the condition_variable handle.  
  
## Syntax  
  
```  
native_handle_type native_handle();  
```  
  
## Return Value  
 `native_handle_type` is defined as a pointer to Concurrency Runtime internal data structures.  
  
## Requirements  
 **Header:** condition_variable  
  
 **Namespace:** std  
  
## See Also  
 [condition_variable Class](../vs140/condition_variable-Class.md)   
 [<condition_variable>](../vs140/-condition_variable-.md)