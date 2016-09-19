---
title: "atomic_fetch_xor Function (C++ AMP)"
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
ms.assetid: 47d1fb7f-94fc-4815-8fe6-0879f13ab8fb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic_fetch_xor Function (C++ AMP)
Atomically peforms an bitwise XOR operation of a value and a memory location.  
  
## Syntax  
  
```  
inline int atomic_fetch_xor(  
   _Inout_ int * _Dest,  
   int _Value                       
) restrict(amp);  
  
inline unsigned int atomic_fetch_xor(  
   _Inout_ unsigned int * _Dest,  
   unsigned int _Value                       
) restrict(amp);  
```  
  
#### Parameters  
 `_Dest`  
 Pointer to the memory location.  
  
 `_Value`  
 The value to use in the XOR calculation.  
  
## Return Value  
 The original value of the memory location.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ Accelerated Massive Parallelism)](../vs140/Concurrency-Namespace--C---AMP-.md)