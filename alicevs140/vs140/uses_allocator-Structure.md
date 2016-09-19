---
title: "uses_allocator Structure"
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
ms.assetid: c418f002-62e9-4806-b70c-41c663cae583
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# uses_allocator Structure
Specializations that always hold true.  
  
## Syntax  
  
```  
template<class Ty, class Alloc>  
struct uses_allocator<promise< Ty>, Alloc> : true_type;  
template<class Ty, class Alloc>  
struct uses_allocator<packaged_task< Ty>, Alloc> : true_type;  
```  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<future\>](../vs140/-future-.md)