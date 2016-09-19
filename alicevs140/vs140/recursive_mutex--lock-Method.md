---
title: "recursive_mutex::lock Method"
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
ms.assetid: c2b07478-b135-475f-8b64-9d3d3aae0fdd
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# recursive_mutex::lock Method
Blocks the calling thread until the thread obtains ownership of the `mutex`.  
  
## Syntax  
  
```cpp  
void lock();  
```  
  
## Remarks  
 If the calling thread already owns the `mutex`, the method returns immediately, and the previous lock remains in effect.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [recursive_mutex Class](../vs140/recursive_mutex-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)