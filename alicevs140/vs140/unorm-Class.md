---
title: "unorm Class"
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
ms.assetid: bc30bd20-6452-4d5f-9158-3b11c4c16ed2
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unorm Class
Represent a unorm number. Each element is a floating point number in the range of [0.0f, 1.0f].  
  
## Syntax  
  
```  
class unorm;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[unorm::unorm Constructor](#unorm__unorm_constructor)|Overloaded. Default constructor. Initialize to 0.0f.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|unorm::operator-- Operator||  
|unorm::operator float Operator|Conversion operator. Convert the unorm number to a floating point value.|  
|unorm::operator*= Operator||  
|unorm::operator/= Operator||  
|unorm::operator++ Operator||  
|unorm::operator+= Operator||  
|unorm::operator= Operator||  
|unorm::operator-= Operator||  
  
## Inheritance Hierarchy  
 `unorm`  
  
## Requirements  
 **Header:** amp_short_vectors.h  
  
 **Namespace:** Concurrency::graphics  
  
##  <a name="unorm__unorm_constructor"></a>  unorm::unorm Constructor  
 Default constructor. Initialize to 0.0f.  
  
```  
unorm(  
   void  
) restrict(amp,cpu);  
explicit unorm(  
   float                 _V  
) restrict(amp,cpu);  
explicit unorm(  
   unsigned int                 _V  
) restrict(amp,cpu);  
explicit unorm(  
   int                 _V  
) restrict(amp,cpu);  
explicit unorm(  
   double                 _V  
) restrict(amp,cpu);  
unorm(  
   const unorm&                 _Other  
) restrict(amp,cpu);  
inline explicit unorm(  
   const norm&                 _Other  
) restrict(amp,cpu);  
```  
  
### Parameters  
 `_V`  
 The value used to initialize.  
  
 `_Other`  
 The norm object used to initialize.  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)