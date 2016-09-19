---
title: "concurrent_unordered_map::operator= Operator"
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
ms.assetid: 9f1a017d-886e-4419-9494-55f937779422
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_map::operator= Operator
Assigns the contents of another `concurrent_unordered_map` object to this one. This method is not concurrency-safe.  
  
## Syntax  
  
```  
concurrent_unordered_map& operator=(  
   const concurrent_unordered_map& _Umap  
);  
  
concurrent_unordered_map& operator=(  
   concurrent_unordered_map&& _Umap  
);  
```  
  
#### Parameters  
 `_Umap`  
 The source `concurrent_unordered_map` object.  
  
## Return Value  
 A reference to this `concurrent_unordered_map` object.  
  
## Remarks  
 After erasing any existing elements a concurrent vector, `operator=` either copies or moves the contents of `_Umap` into the concurrent vector.  
  
## Requirements  
 **Header:** concurrent_unordered_map.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_map Class](../vs140/concurrent_unordered_map-Class.md)