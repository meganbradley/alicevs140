---
title: "unique_lock::owns_lock Method"
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
ms.assetid: 666b8fad-6353-4222-9a40-dec6eb353c46
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique_lock::owns_lock Method
Specifies whether the calling thread owns the associated `mutex`.  
  
## Syntax  
  
```cpp  
bool owns_lock() const _NOEXCEPT;  
```  
  
## Return Value  
 `true` if the thread owns the `mutex`; otherwise, `false`.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [unique_lock Class](../vs140/unique_lock-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)