---
title: "concurrent_vector::grow_by Method"
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
ms.assetid: 3aef8f98-e5a8-40a6-8db8-91315f41dadc
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_vector::grow_by Method
Grows this concurrent vector by `_Delta` elements. This method is concurrency-safe.  
  
## Syntax  
  
```  
iterator grow_by(  
   size_type _Delta  
);  
  
iterator grow_by(  
   size_type _Delta,  
   const_reference _Item  
);  
```  
  
#### Parameters  
 `_Delta`  
 The number of elements to append to the object.  
  
 `_Item`  
 The value to initialize the new elements with.  
  
## Return Value  
 An iterator to first item appended.  
  
## Remarks  
 If `_Item` is not specified, the new elements are default constructed.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)