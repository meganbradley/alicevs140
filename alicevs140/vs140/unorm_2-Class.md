---
title: "unorm_2 Class"
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
ms.assetid: 62e88ea7-e29f-4f62-95ce-61a1f39f5e34
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unorm_2 Class
Represents a short vector of two unsigned normal numbers.  
  
## Syntax  
  
```  
class unorm_2;  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`value_type`||  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[unorm_2::unorm_2 Constructor](#unorm_2__unorm_2_constructor)|Overloaded. Default constructor, initializes all elements with 0.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|unorm_2::get_x Method||  
|unorm_2::get_xy Method||  
|unorm_2::get_y Method||  
|unorm_2::get_yx Method||  
|unorm_2::ref_g Method||  
|unorm_2::ref_r Method||  
|unorm_2::ref_x Method||  
|unorm_2::ref_y Method||  
|unorm_2::set_x Method||  
|unorm_2::set_xy Method||  
|unorm_2::set_y Method||  
|unorm_2::set_yx Method||  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|unorm_2::operator-- Operator||  
|unorm_2::operator*= Operator||  
|unorm_2::operator/= Operator||  
|unorm_2::operator++ Operator||  
|unorm_2::operator+= Operator||  
|unorm_2::operator= Operator||  
|unorm_2::operator-= Operator||  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|unorm_2::size Constant||  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|unorm_2::g Data Member||  
|unorm_2::gr Data Member||  
|unorm_2::r Data Member||  
|unorm_2::rg Data Member||  
|unorm_2::x Data Member||  
|unorm_2::xy Data Member||  
|unorm_2::y Data Member||  
|unorm_2::yx Data Member||  
  
## Inheritance Hierarchy  
 `unorm_2`  
  
## Requirements  
 **Header:** amp_short_vectors.h  
  
 **Namespace:** Concurrency::graphics  
  
##  <a name="unorm_2__unorm_2_constructor"></a>  unorm_2::unorm_2 Constructor  
 Default constructor, initializes all elements with 0.  
  
```  
unorm_2() restrict(amp,cpu);  
unorm_2(  
   unorm                 _V0,  
   unorm                 _V1  
) restrict(amp,cpu);  
unorm_2(  
   float                 _V0,  
   float                 _V1  
) restrict(amp,cpu);  
unorm_2(  
   unorm                 _V  
) restrict(amp,cpu);  
explicit unorm_2(  
   float                 _V  
) restrict(amp,cpu);  
unorm_2(  
   const unorm_2&                 _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const uint_2&                 _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const int_2&                 _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const float_2&                 _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const norm_2&                 _Other  
) restrict(amp,cpu);  
explicit inline unorm_2(  
   const double_2&                 _Other  
) restrict(amp,cpu);  
```  
  
### Parameters  
 `_V0`  
 The value to initialize element 0.  
  
 `_V1`  
 The value to initialize element 1.  
  
 `_V`  
 The value for initialization.  
  
 `_Other`  
 The object used to initialize.  
  
##  <a name="unorm_2__size_constant"></a>  unorm_2::size Constant  
  
```  
static const int size = 2;  
```  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)