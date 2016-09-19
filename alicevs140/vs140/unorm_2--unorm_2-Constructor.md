---
title: "unorm_2::unorm_2 Constructor"
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
ms.assetid: fc80635d-9195-4507-9779-9ea785a0b4f6
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unorm_2::unorm_2 Constructor
Default constructor, initializes all elements with 0.  
  
## Syntax  
  
```  
unorm_2() restrict(amp,cpu);  
unorm_2(  
   unorm _V0,  
   unorm _V1  
) restrict(amp,cpu);  
unorm_2(  
   float _V0,  
   float _V1  
) restrict(amp,cpu);  
unorm_2(  
   unorm _V  
) restrict(amp,cpu);  
explicit unorm_2(  
   float _V  
) restrict(amp,cpu);  
unorm_2(  
   const unorm_2& _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const uint_2& _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const int_2& _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const float_2& _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const norm_2& _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const double_2& _Other  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_V0`  
 The value to initialize element 0.  
  
 `_V1`  
 The value to initialize element 1.  
  
 `_V`  
 The value for initialization.  
  
 `_Other`  
 The object used to initialize.  
  
## Requirements  
 **Header:** amp_short_vectors.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [unorm_2 Class](../vs140/unorm_2-Class.md)