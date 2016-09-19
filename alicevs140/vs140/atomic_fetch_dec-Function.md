---
title: "atomic_fetch_dec Function"
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
ms.assetid: 0af9113f-6c31-47ab-a9bf-7170a965e982
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic_fetch_dec Function
Atomically decrements the value stored at the specified memory location.  
  
## Syntax  
  
```  
inline int atomic_fetch_dec(  
   _Inout_ int * _Dest  
) restrict(amp);  
  
inline unsigned int atomic_fetch_dec(  
   _Inout_ unsigned int * _Dest  
) restrict(amp);  
```  
  
#### Parameters  
 `_Dest`  
 The location in memory of the value to be decremented.  
  
## Return Value  
 The original value stored at the memory location.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ Accelerated Massive Parallelism)](../vs140/Concurrency-Namespace--C---AMP-.md)