---
title: "unique_lock::~unique_lock Destructor"
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
ms.assetid: f11d2c70-5d28-4cbf-95c9-596a9a3f163f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique_lock::~unique_lock Destructor
Releases any resources that are associated with the `unique_lock` object.  
  
## Syntax  
  
```cpp  
~unique_lock() _NOEXCEPT;  
```  
  
## Remarks  
 If the calling thread owns the associated `mutex`, the destructor releases ownership by calling unlock on the `mutex` object.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [unique_lock Class](../vs140/unique_lock-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)