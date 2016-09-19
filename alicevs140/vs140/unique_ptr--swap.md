---
title: "unique_ptr::swap"
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
ms.assetid: d8622042-43da-4c22-858d-736803359702
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique_ptr::swap
Exchanges pointers between two `unique_ptr` objects.  
  
## Syntax  
  
```  
void swap(unique_ptr& _Right);  
```  
  
#### Parameters  
 `_Right`  
 A `unique_ptr` used to swap pointers.  
  
## Remarks  
 The member function swaps `stored_ptr` with `right.stored_ptr` and `stored_deleter` with `right.stored_deleter`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [unique_ptr Class](../vs140/unique_ptr-Class.md)   
 [<memory\>](../vs140/-memory-.md)   
 [Thread Safety in the C++ Standard Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)