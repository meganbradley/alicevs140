---
title: "initializer_list::begin"
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
ms.assetid: 3ff920ea-cbe5-4da8-b29a-06769dadf7ca
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# initializer_list::begin
Returns a pointer to the first element in an `initializer_list`.  
  
## Syntax  
  
```  
constexpr const InputIterator* begin() const noexcept;  
```  
  
## Return Value  
 A pointer to the first element of the `initializer_list`. If the list is empty, the pointer is the same for the beginning and end of the list.  
  
## Remarks  
  
## Requirements  
 **Header:** <initializer_list>  
  
 **Namespace:** std  
  
## See Also  
 [initializer_list Class](../vs140/initializer_list-Class.md)