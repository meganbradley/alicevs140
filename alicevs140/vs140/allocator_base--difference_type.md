---
title: "allocator_base::difference_type"
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
ms.assetid: e3a5f646-b5fa-4d99-bf3c-439c034610d6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator_base::difference_type
A signed integral type that can represent the difference between values of pointers to the type of object managed by the allocator.  
  
## Syntax  
  
```  
typedef std::ptrdiff_t difference_type;  
```  
  
## Remarks  
 The integer type implements  as a typedef for `std::ptrdiff_t`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext