---
title: "double_2 Class"
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
ms.assetid: c19c2d21-3cbf-4ce5-b460-3b8253688f82
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# double_2 Class
Represent a short vector of 2 double's.  
  
## Syntax  
  
```  
class double_2;  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`value_type`||  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[double_2::double_2 Constructor](#double_2__double_2_constructor)|Overloaded. Default constructor, initializes all elements with 0.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|double_2::get_x Method||  
|double_2::get_xy Method||  
|double_2::get_y Method||  
|double_2::get_yx Method||  
|double_2::ref_g Method||  
|double_2::ref_r Method||  
|double_2::ref_x Method||  
|double_2::ref_y Method||  
|double_2::set_x Method||  
|double_2::set_xy Method||  
|double_2::set_y Method||  
|double_2::set_yx Method||  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|double_2::operator- Operator||  
|double_2::operator-- Operator||  
|double_2::operator*= Operator||  
|double_2::operator/= Operator||  
|double_2::operator++ Operator||  
|double_2::operator+= Operator||  
|double_2::operator= Operator||  
|double_2::operator-= Operator||  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|double_2::size Constant||  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|double_2::g Data Member||  
|double_2::gr Data Member||  
|double_2::r Data Member||  
|double_2::rg Data Member||  
|double_2::x Data Member||  
|double_2::xy Data Member||  
|double_2::y Data Member||  
|double_2::yx Data Member||  
  
## Inheritance Hierarchy  
 `double_2`  
  
## Requirements  
 **Header:** amp_short_vectors.h  
  
 **Namespace:** Concurrency::graphics  
  
##  <a name="double_2__double_2_constructor"></a>  double_2::double_2 Constructor  
 Default constructor, initializes all elements with 0.  
  
```  
double_2() restrict(amp,cpu);  
double_2(  
   double                 _V0,  
   double                 _V1  
) restrict(amp,cpu);  
double_2(  
   double                 _V  
) restrict(amp,cpu);  
double_2(  
   const double_2&                 _Other  
) restrict(amp,cpu);  
explicit inline double_2(  
   const uint_2&                 _Other  
) restrict(amp,cpu);  
explicit inline double_2(  
   const int_2&                 _Other  
) restrict(amp,cpu);  
explicit inline double_2(  
   const float_2&                 _Other  
) restrict(amp,cpu);  
explicit inline double_2(  
   const unorm_2&                 _Other  
) restrict(amp,cpu);  
explicit inline double_2(  
   const norm_2&                 _Other  
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
  
##  <a name="double_2__size_constant"></a>  double_2::size Constant  
  
```  
static const int size = 2;  
```  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)