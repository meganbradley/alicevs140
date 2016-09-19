---
title: "concurrent_unordered_set::unsafe_begin Method"
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
ms.assetid: 0f0a0049-6306-4565-bbb1-30e4846411f7
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_set::unsafe_begin Method
Returns an iterator to the first element in this container for a specific bucket.  
  
## Syntax  
  
```  
local_iterator unsafe_begin(  
   size_type _Bucket  
);  
  
const_local_iterator unsafe_begin(  
   size_type _Bucket  
) const;  
```  
  
#### Parameters  
 `_Bucket`  
 The bucket index.  
  
## Return Value  
 An iterator pointing to the beginning of the bucket.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_set Class](../vs140/concurrent_unordered_set-Class.md)