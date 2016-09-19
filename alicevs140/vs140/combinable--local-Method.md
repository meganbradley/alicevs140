---
title: "combinable::local Method"
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
ms.assetid: 496c298e-f159-44f3-8c25-ebf8f5b175be
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# combinable::local Method
Returns a reference to the thread-private sub-computation.  
  
## Syntax  
  
```  
_Ty& local();  
  
_Ty& local(  
   bool& _Exists  
);  
```  
  
#### Parameters  
 `_Exists`  
 A reference to a boolean. The boolean value referenced by this argument will be set to `true` if the sub-computation already existed on this thread, and set to `false` if this was the first sub-computation on this thread.  
  
## Return Value  
 A reference to the thread-private sub-computation.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [combinable Class](../vs140/combinable-Class.md)   
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)