---
title: "set::allocator_type"
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
ms.assetid: f79a57ca-7d8f-4378-9c91-e6a95b2a9e65
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::allocator_type
A type that represents the allocator class for the set object.  
  
## Syntax  
  
```  
typedef Allocator allocator_type;  
```  
  
## Remarks  
 **allocator_type** is a synonym for the template parameter [Allocator](../vs140/set-Class.md).  
  
 Returns the function object that a multiset uses to order its elements, which is the template parameter `Allocator`.  
  
 For more information on `Allocator`, see the Remarks section of the [set Class](../vs140/set-Class.md) topic.  
  
## Example  
 See the example for [get_allocator](../vs140/set--get_allocator.md) for an example that uses `allocator_type`.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)