---
title: "error_code::message"
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
ms.assetid: 70719485-5f44-4b98-8c82-6114b7c9c676
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# error_code::message
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
 [error_code Class](../vs140/error_code-Class.md)