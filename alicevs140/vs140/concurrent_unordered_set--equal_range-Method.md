---
title: "concurrent_unordered_set::equal_range Method"
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
ms.assetid: e1d90a02-a309-4ed7-a480-9bbfa70b429d
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_set::equal_range Method
Finds a range that matches a specified key. This function is concurrency safe.  
  
## Syntax  
  
```  
std::pair<iterator, iterator> equal_range(  
   const key_type& _Keyval  
);  
  
std::pair<const_iterator, const_iterator> equal_range(  
   const key_type& _Keyval  
) const;  
```  
  
#### Parameters  
 `_Keyval`  
 The key value to search for.  
  
## Return Value  
 A [pair](assetId:///32e72d66-3020-4cb9-92c3-f7a5fa7998ff) where the first element is an iterator to the beginning and the second element is an iterator to the end of the range.  
  
## Remarks  
 It is possible for concurrent inserts to cause additional keys to be inserted after the begin iterator and before the end iterator.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_set Class](../vs140/concurrent_unordered_set-Class.md)