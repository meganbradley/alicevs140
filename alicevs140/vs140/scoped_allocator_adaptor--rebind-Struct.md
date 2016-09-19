---
title: "scoped_allocator_adaptor::rebind Struct"
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
ms.assetid: 4b8ff12f-1af3-4922-95bb-68e13b8b63e4
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scoped_allocator_adaptor::rebind Struct
Defines the type `Outer::rebind<Other>::other` as a synonym for `scoped_allocator_adaptor<Other, Inner...>`.  
  
## Syntax  
  
```cpp  
template<class Other>  
   struct rebind{  
      typedef Other_traits::rebind<Other> Other_alloc;  
      typedef scoped_allocator_adaptor<Other_alloc, Inner...> other;  
  
   };  
```  
  
## Requirements  
 **Header:** <scoped_allocator>  
  
 **Namespace:** std  
  
## See Also  
 [scoped_allocator_adaptor Class](../vs140/scoped_allocator_adaptor-Class.md)