---
title: "scoped_allocator_adaptor::destroy Method"
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
ms.assetid: 7d858127-d96a-41b9-8e42-49cbaf6ac8bf
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scoped_allocator_adaptor::destroy Method
Destroys a specified object.  
  
## Syntax  
  
```cpp  
template<class Ty>  
   void destroy(Ty *ptr)  
```  
  
#### Parameters  
 `ptr`  
 A pointer to the object to be destroyed.  
  
## Return Value  
 `Outermost_traits::destroy(OUTERMOST(*this), ptr)`  
  
## Requirements  
 **Header:** <scoped_allocator>  
  
 **Namespace:** std  
  
## See Also  
 [scoped_allocator_adaptor Class](../vs140/scoped_allocator_adaptor-Class.md)   
 [allocator_traits::destroy Method](../vs140/allocator_traits--destroy-Method.md)