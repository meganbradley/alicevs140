---
title: "concurrent_unordered_multimap::rehash Method"
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
ms.assetid: d8cbb177-7870-49b0-b436-9644ca0c6c67
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_multimap::rehash Method
Rebuilds the hash table.  
  
## Syntax  
  
```  
void rehash(  
   size_type _Buckets  
);  
```  
  
#### Parameters  
 `_Buckets`  
 The desired number of buckets.  
  
## Remarks  
 The member function alters the number of buckets to be at least `_Buckets` and rebuilds the hash table as needed. The number of buckets must be a power of 2. If not a power of 2, it will be rounded up to the next largest power of 2.  
  
 It throws an [out_of_range](../vs140/out_of_range-Class.md) exception if the number of buckets is invalid (either 0 or greater than the maximum number of buckets).  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_multimap Class](../vs140/concurrent_unordered_multimap-Class.md)