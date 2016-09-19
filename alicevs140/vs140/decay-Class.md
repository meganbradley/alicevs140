---
title: "decay Class"
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
ms.assetid: 96baa2fd-c8e0-49af-be91-ba375ba7f9dc
caps.latest.revision: 20
translation.priority.mt: 
  - de-de
  - ja-jp
---
# decay Class
Produces the type as passed by value. Makes the type non-reference, non-const, non-volatile, or makes a pointer to the type from a function or an array type.  
  
## Syntax  
  
```  
template<class T>  
    struct decay;  
  
template<class T> using decay_t = typename decay<T>::type;  
```  
  
#### Parameters  
 `T`  
 The type to modify.  
  
## Remarks  
 Use the decay template to produce the resulting type as if the type was passed by value as an argument. The template class member typedef `type` holds a modified type that is defined in the following stages:  
  
-   The type `U` is defined as `remove_reference<T>::type`.  
  
-   If `is_array<U>::value` is true, the modified type `type` is `remove_extent<U>::type *`.  
  
-   Otherwise, if `is_function<U>::value` is true, the modified type `type` is `add_pointer<U>::type`.  
  
-   Otherwise, the modified type `type` is `remove_cv<U>::type`.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)