---
title: "default_delete"
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
ms.assetid: a9ccba42-1d0c-4f2d-b055-e7d506190e9b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# default_delete
Deletes objects allocated with `operator new`. Suitable for use with `unique_ptr`.  
  
## Syntax  
  
```  
template<class T>    struct default_delete {        constexpr default_delete() noexcept = default;         template<class Other,                     class = typename enable_if<is_convertible< Other*, T*>::value, void>::type>>  
            default_delete(                const default_delete<Other>&            ) noexcept;         void operator()(T*Ptr) const noexcept;     };  
  
template<class T>    struct default_delete<T[]>    {        constexpr default_delete() noexcept = default;    template<class Other,     class = typename enable_if<is_convertible<Other(*)[], T(*)[]>::value, void>::type>        default_delete(const default_delete<Other[]>&) noexcept    template<class Other,      class = typename enable_if<is_convertible<Other(*)[], T(*)[]>::value, void>::type>        void operator()(Other*) const noexcept;    };  
```  
  
#### Parameters  
 `Ptr`  
 Pointer to the object to delete.  
  
 Other  
 The type of elements in the array to be deleted.  
  
## Exceptions  
  
## Remarks  
 The template class describes a `deleter` that deletes scalar objects allocated with `operator new`, suitable for use with template class `unique_ptr`. It also has the explicit specialization `default_delete<Type[]>`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [<memory\>](../vs140/-memory-.md)