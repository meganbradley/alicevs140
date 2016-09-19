---
title: "error_condition::message"
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
ms.assetid: 422a45ef-008c-48f9-ab79-041c4af6b898
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_condition::message
Returns the name of the error code.  
  
## Syntax  
  
```  
string message() const;  
```  
  
## Return Value  
 A `string` representing the name of the error code.  
  
## Remarks  
 This member function returns `category().message(value())`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_condition Class](../vs140/error_condition-Class.md)