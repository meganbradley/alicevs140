---
title: "pointer_traits Struct"
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
ms.assetid: 545aecf1-3561-4859-8b34-603c079fe1b3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pointer_traits Struct
Supplies information that is needed by an object of template class `allocator_traits` to describe an allocator with pointer type `Ptr`.  
  
## Syntax  
  
```cpp  
template<class Ptr>  
    struct pointer_traits;  
```  
  
## Remarks  
 Ptr can be a raw pointer of type `Ty *` or a class with the following properties.  
  
```  
template<class Ty, class... Rest>  
    struct Ptr  
    { // describes a pointer type usable by allocators  
    typedef Ptr pointer;  
    typedef T1 element_type; // optional  
    typedef T2 difference_type; // optional  
    template<class Other>  
        using rebind = typename Ptr<Other, Rest...>; // optional  
  
    static pointer pointer_to(element_type& obj); // optional  
    };  
```  
  
### Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`typedef T2 difference_type`|The type `T2` is `Ptr::difference_type` if that type exists, otherwise `ptrdiff_t`. If `Ptr` is a raw pointer, the type is `ptrdiff_t`.|  
|`typedef T1 element_type`|The type `T1` is `Ptr::element_type` if that type exists, otherwise `Ty`. If `Ptr` is a raw pointer, the type is `Ty`.|  
|`typedef Ptr pointer`|The type is `Ptr`.|  
  
### Structs  
  
|Name|Description|  
|----------|-----------------|  
|`pointer_traits::rebind`|Attempts to convert the underlying pointer type to a specified type.|  
  
### Methods  
  
|Name|Description|  
|----------|-----------------|  
|[pointer_traits_pointer_to](#pointer_traits__pointer_to_method)|Converts an arbitrary reference to an object of class `Ptr`.|  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
##  <a name="pointer_traits__pointer_to_method"></a>  pointer_traits::pointer_to Method  
 Static method that returns `Ptr::pointer_to(obj)`, if that function exists. Otherwise, it is not possible to convert an arbitrary reference to an object of class `Ptr`. If `Ptr` is a raw pointer, this method returns `addressof(obj)`.  
  
```cpp  
static pointer pointer_to(element_type& obj);  
```  
  
## See Also  
 [<memory\>](../vs140/-memory-.md)   
 [allocator_traits Class](../vs140/allocator_traits-Class.md)