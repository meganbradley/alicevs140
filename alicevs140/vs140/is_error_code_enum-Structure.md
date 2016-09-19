---
title: "is_error_code_enum Structure"
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
ms.assetid: 84ae4b99-66d2-41ba-9b50-645fcbe14630
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# is_error_code_enum Structure
Specialization that indicates that [future_errc](../vs140/-future--enums.md#future_errc_enumeration) is suitable for storing an [error_code](../vs140/error_code-Class.md).  
  
## Syntax  
  
```  
template<>  
struct is_error_code_enum<Future_errc> : public true_type;  
```  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<future\>](../vs140/-future-.md)