---
title: "error_code::operator bool"
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
ms.assetid: 2d1db2f8-a7a7-46d6-b20f-d1d5a24b55e1
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_code::operator bool
Casts a variable of type `error_code`.  
  
## Syntax  
  
```  
explicit operator bool() const;  
```  
  
## Return Value  
 The Boolean value of the `error_code` object.  
  
## Remarks  
 The operator returns a value convertible to `true` only if [value](../vs140/error_code--value.md) is not equal to zero. The return type is convertible only to `bool`, not to `void *` or other known scalar types.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_code Class](../vs140/error_code-Class.md)