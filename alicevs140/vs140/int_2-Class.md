---
title: "int_2 Class"
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
ms.assetid: 258b02e9-f1ee-46c2-8edd-dc9f69184846
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# int_2 Class
Represents a short vector of two integers.  
  
## Syntax  
  
```  
class int_2;  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`value_type`||  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[int_2::int_2 Constructor](#int_2__int_2_constructor)|Overloaded. Default constructor, initializes all elements with 0.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|int_2::get_x Method||  
|int_2::get_xy Method||  
|int_2::get_y Method||  
|int_2::get_yx Method||  
|int_2::ref_g Method||  
|int_2::ref_r Method||  
|int_2::ref_x Method||  
|int_2::ref_y Method||  
|int_2::set_x Method||  
|int_2::set_xy Method||  
|int_2::set_y Method||  
|int_2::set_yx Method||  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|int_2::operator- Operator||  
|int_2::operator-- Operator||  
|int_2::operator%= Operator||  
|int_2::operator&= Operator||  
|int_2::operator*= Operator||  
|int_2::operator/= Operator||  
|int_2::operator^= Operator||  
|int_2::operator&#124;= Operator||  
|int_2::operator~ Operator||  
|int_2::operator++ Operator||  
|int_2::operator+= Operator||  
|int_2::operator<<= Operator||  
|int_2::operator= Operator||  
|int_2::operator-= Operator||  
|int_2::operator>>= Operator||  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|[int_2::size Constant](#int_2__size_constant)||  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|int_2::g Data Member||  
|int_2::gr Data Member||  
|int_2::r Data Member||  
|int_2::rg Data Member||  
|int_2::x Data Member||  
|int_2::xy Data Member||  
|int_2::y Data Member||  
|int_2::yx Data Member||  
  
## Inheritance Hierarchy  
 `int_2`  
  
## Requirements  
 **Header:** amp_short_vectors.h  
  
 **Namespace:** Concurrency::graphics  
  
##  <a name="int_2__int_2_constructor"></a>  int_2::int_2 Constructor  
 Default constructor, initializes all elements with 0.  
  
```  
int_2() restrict(amp,cpu);  
int_2(  
   int                 _V0,  
   int                 _V1  
) restrict(amp,cpu);  
int_2(  
   int                 _V  
) restrict(amp,cpu);  
int_2(  
   const int_2&                 _Other  
) restrict(amp,cpu);  
explicit inline int_2(  
   const uint_2&                 _Other  
) restrict(amp,cpu);  
explicit inline int_2(  
   const float_2&                 _Other  
) restrict(amp,cpu);  
explicit inline int_2(  
   const unorm_2&                 _Other  
) restrict(amp,cpu);  
explicit inline int_2(  
   const norm_2&                 _Other  
) restrict(amp,cpu);  
explicit inline int_2(  
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
  
##  <a name="int_2__size_constant"></a>  int_2::size Constant  
  
```  
static const int size = 2;  
```  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)