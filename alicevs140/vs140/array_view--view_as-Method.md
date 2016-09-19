---
title: "array_view::view_as Method"
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
ms.assetid: c6ba6ad6-2a9b-4077-b82a-f1027ca945da
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array_view::view_as Method
Reinterprets this `array_view` as an `array_view` of a different rank.  
  
## Syntax  
  
```  
template <  
   int _New_rank  
>  
array_view<_Value_type,_New_rank> view_as(  
   const Concurrency::extent<_New_rank>& _View_extent  
) const restrict(amp,cpu);  
  
template <  
   int _New_rank  
>  
array_view<const _Value_type,_New_rank> view_as(  
   const Concurrency::extent<_New_rank> _View_extent  
) const restrict(amp,cpu);  
```  
  
#### Parameters  
 `_New_rank`  
 The rank of the new `array_view` object.  
  
 `_View_extent`  
 The reshaping `extent`.  
  
 `_Value_type`  
 The data type of the elements in both the original [array](../vs140/array-Class.md) object and the returned `array_view` object.  
  
## Return Value  
 The [array_view](../vs140/array_view-Class.md) object that is constructed.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array_view Class](../vs140/array_view-Class.md)