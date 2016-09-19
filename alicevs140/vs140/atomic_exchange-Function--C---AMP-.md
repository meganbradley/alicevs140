---
title: "atomic_exchange Function (C++ AMP)"
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
ms.assetid: 4ef0f6de-b32e-4b76-be07-fd8e0bd01333
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic_exchange Function (C++ AMP)
Sets the value of destination location as an atomic operation.  
  
## Syntax  
  
```  
inline int atomic_exchange(  
   _Inout_ int * _Dest,  
   int _Value                       
) restrict(amp);  
  
inline unsigned int atomic_exchange(  
   _Inout_ unsigned int * _Dest,  
   unsigned int _Value                       
) restrict(amp);  
  
inline float atomic_exchange(  
   _Inout_ float * _Dest,  
   float _Value                       
) restrict(amp);  
```  
  
#### Parameters  
 `_Dest`  
 Pointer to the destionation location.  
  
 `_Value`  
 The new value.  
  
## Return Value  
 The original value of the destination location.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ Accelerated Massive Parallelism)](../vs140/Concurrency-Namespace--C---AMP-.md)