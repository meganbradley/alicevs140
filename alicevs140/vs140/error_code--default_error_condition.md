---
title: "error_code::default_error_condition"
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
ms.assetid: fdb140f2-58dd-4c1a-a15d-52ab66614d0c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_code::default_error_condition
Returns the default error condition.  
  
## Syntax  
  
```  
error_condition default_error_condition() const;  
```  
  
## Return Value  
 The [error_condition](../vs140/error_condition-Class.md) specified by [default_error_condition](../vs140/error_category--default_error_condition.md).  
  
## Remarks  
 This member function returns `category().default_error_condition(value())`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_code Class](../vs140/error_code-Class.md)