---
title: "error_code::clear"
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
ms.assetid: df9e228a-e173-4dd7-9be4-eb2cfd68a394
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_code::clear
Clears the error code value and category.  
  
## Syntax  
  
```  
clear();  
```  
  
## Remarks  
 The member function stores a zero error code value and a pointer to the [generic_category](../vs140/generic_category.md) object.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)   
 [error_code Class](../vs140/error_code-Class.md)