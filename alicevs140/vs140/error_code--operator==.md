---
title: "error_code::operator=="
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
ms.assetid: 288945c7-7b18-443e-90ba-49a25bbd1123
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_code::operator==
Tests for equality between `error_code` objects.  
  
## Syntax  
  
```  
bool operator==(const error_code& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The object to be tested for equality.|  
  
## Return Value  
 **true** if the objects are equal; **false** if objects are not equal.  
  
## Remarks  
 The member operator returns `category() == _Right.category() && value == _Right.value()`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_code Class](../vs140/error_code-Class.md)