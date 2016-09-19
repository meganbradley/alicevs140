---
title: "texture_view::gather_red Method"
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
ms.assetid: 817d86bb-ad16-47f2-87ea-cbdaf44acb79
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# texture_view::gather_red Method
Samples the texture at the specified coordinates by using the specified sampling configuration and returns the red (x) components of the four sampled texels.  
  
## Syntax  
  
```  
const gather_return_type gather_red(  
   const sampler& _Sampler,  
   const coordinates_type& _Coord  
) const restrict(amp);  
  
template<  
   address_mode _Address_mode = address_clamp  
>  
const gather_return_type gather_red(  
   const coordinates_type& _Coord  
) const restrict(amp);  
```  
  
#### Parameters  
 `_Address_mode`  
 The address mode to use to sample the `texture_view`. The address mode is the same for all dimensions.  
  
 `_Sampler`  
 The sampler configuration to use to sample the `texture_view`.  
  
 `_Coord`  
 The coordinates to take the sample from. Fractional coordinate values are used to interpolate between sample texels.  
  
## Return Value  
 A rank 4 short vector containing the red (x) component of the 4 sampled texel values.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** concurrency::graphics  
  
## See Also  
 [texture_view Class](../vs140/texture_view-Class.md)