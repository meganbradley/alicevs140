---
title: "concurrent_unordered_set::find Method"
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
ms.assetid: 0c203849-798c-4ee0-85b9-3665c54e4d8b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_set::find Method
Finds an element that matches a specified key. This function is concurrency safe.  
  
## Syntax  
  
```  
iterator find(  
   const key_type& _Keyval  
);  
  
const_iterator find(  
   const key_type& _Keyval  
) const;  
```  
  
#### Parameters  
 `_Keyval`  
 The key value to search for.  
  
## Return Value  
 An iterator pointing to the location of the the first element that matched the key provided, or the iterator `end()` if no such element exists.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_set Class](../vs140/concurrent_unordered_set-Class.md)