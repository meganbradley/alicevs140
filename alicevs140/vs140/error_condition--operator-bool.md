---
title: "error_condition::operator bool"
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
ms.assetid: d8170da9-d26f-4206-814a-984a7694d942
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_condition::operator bool
Casts a variable of type `error_condition`.  
  
## Syntax  
  
```  
explicit operator bool() const;  
```  
  
## Return Value  
 The Boolean value of the `error_condition` object.  
  
## Remarks  
 The operator returns a value convertible to `true` only if [value](../vs140/error_condition--value.md) is not equal to zero. The return type is convertible only to `bool`, not to `void *` or other known scalar types.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_condition Class](../vs140/error_condition-Class.md)