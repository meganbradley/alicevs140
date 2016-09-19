---
title: "concurrent_unordered_multiset::unsafe_bucket_size Method"
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
ms.assetid: bb92f948-691f-4de1-bae8-f6654d20f10f
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_multiset::unsafe_bucket_size Method
Returns the number of items in a specific bucket of this container.  
  
## Syntax  
  
```  
size_type unsafe_bucket_size(  
   size_type _Bucket  
);  
```  
  
#### Parameters  
 `_Bucket`  
 The bucket to search for.  
  
## Return Value  
 The current number of buckets in this container.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_multiset Class](../vs140/concurrent_unordered_multiset-Class.md)