---
title: "atomic_compare_exchange Function"
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
ms.assetid: 3349f83f-ff21-48ee-8c91-09207877e98c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic_compare_exchange Function
Atomically compares the value stored at a memory location specified in the first argument for equality with the value of the second specified argument, and if the values are the same, the value at the memory location is changed to that of the third specified argument.  
  
## Syntax  
  
```  
inline bool atomic_compare_exchange(  
   _Inout_ int * _Dest,  
   _Inout_ int * _Expected_value,  
   int _Value  
) restrict(amp);  
  
inline bool atomic_compare_exchange(  
   _Inout_ unsigned int * _Dest,  
   _Inout_ unsigned int * _Expected_value,  
   unsigned int _Value  
) restrict(amp);  
```  
  
#### Parameters  
 `_Dest`  
 The location from which one of the values to be compared is read, and to which the new value, if any, is to be stored.  
  
 `_Expected_value`  
 The location from which the second value to be compared is read.  
  
 `_Value`  
 The value to be stored to the memory location specified in by `_Dest` if `_Dest` is equal to `_Expected_value`.  
  
## Return Value  
 `true` if the operation is successful; otherwise, `false`.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ Accelerated Massive Parallelism)](../vs140/Concurrency-Namespace--C---AMP-.md)