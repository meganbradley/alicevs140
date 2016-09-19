---
title: "allocator_base::const_pointer"
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
ms.assetid: 9a4b4ea5-d681-4a3f-8069-f20370bc05bc
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator_base::const_pointer
A type that provides a constant pointer to the type of object managed by the allocator.  
  
## Syntax  
  
```  
typedef const Type *const_pointer;  
```  
  
## Remarks  
 The pointer type implements  as a typedef for `const Type*`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext