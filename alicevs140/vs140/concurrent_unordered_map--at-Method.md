---
title: "concurrent_unordered_map::at Method"
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
ms.assetid: e64bf194-8ea3-4344-bbbd-73d528394654
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_map::at Method
Finds an element in a `concurrent_unordered_map` with a specified key value.. This method is concurrency-safe.  
  
## Syntax  
  
```  
mapped_type& at(  
   const key_type& _Keyval  
);  
  
const mapped_type& at(  
   const key_type& _Keyval  
) const;  
```  
  
#### Parameters  
 `_Keyval`  
 The key value to find.  
  
## Return Value  
 A reference to the data value of the element found.  
  
## Remarks  
 If the argument key value is not found, the function throws an object of class `out_of_range`.  
  
## Requirements  
 **Header:** concurrent_unordered_map.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_map Class](../vs140/concurrent_unordered_map-Class.md)