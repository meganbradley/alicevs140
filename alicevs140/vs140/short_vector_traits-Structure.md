---
title: "short_vector_traits Structure"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cd9492da-9e02-4a6e-9d50-b61252cdb460
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# short_vector_traits Structure
short_vector_traits allows retrival of the underlying vector length and scalar type of a short vector type or a scalar type  
  
## Syntax  
  
```  
template<  
   typename             _Type  
>  
struct short_vector_traits;  
template<>  
struct short_vector_traits<unsigned int>;  
template<>  
struct short_vector_traits<uint_2>;  
template<>  
struct short_vector_traits<uint_3>;  
template<>  
struct short_vector_traits<uint_4>;  
template<>  
struct short_vector_traits<int>;  
template<>  
struct short_vector_traits<int_2>;  
template<>  
struct short_vector_traits<int_3>;  
template<>  
struct short_vector_traits<int_4>;  
template<>  
struct short_vector_traits<float>;  
template<>  
struct short_vector_traits<float_2>;  
template<>  
struct short_vector_traits<float_3>;  
template<>  
struct short_vector_traits<float_4>;  
template<>  
struct short_vector_traits<unorm>;  
template<>  
struct short_vector_traits<unorm_2>;  
template<>  
struct short_vector_traits<unorm_3>;  
template<>  
struct short_vector_traits<unorm_4>;  
template<>  
struct short_vector_traits<norm>;  
template<>  
struct short_vector_traits<norm_2>;  
template<>  
struct short_vector_traits<norm_3>;  
template<>  
struct short_vector_traits<norm_4>;  
template<>  
struct short_vector_traits<double>;  
template<>  
struct short_vector_traits<double_2>;  
template<>  
struct short_vector_traits<double_3>;  
template<>  
struct short_vector_traits<double_4>;  
```  
  
#### Parameters  
 `_Type`  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`value_type`||  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[short_vector_traits::short_vector_traits Constructor](#short_vector_traits__short_vector_traits_constructor)||  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|[short_vector_traits::size Constant](#short_vector_traits__size_constant)||  
  
## Inheritance Hierarchy  
 `short_vector_traits`  
  
## Requirements  
 **Header:** amp_short_vectors.h  
  
 **Namespace:** Concurrency::graphics  
  
##  <a name="short_vector_traits__short_vector_traits_constructor"></a>  short_vector_traits::short_vector_traits Constructor  
  
```  
short_vector_traits();  
```  
  
##  <a name="short_vector_traits__size_constant"></a>  short_vector_traits::size Constant  
  
```  
static int const size = 1;  
```  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)