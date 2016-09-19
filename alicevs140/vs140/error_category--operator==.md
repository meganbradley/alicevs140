---
title: "error_category::operator=="
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
ms.assetid: db62bb1c-3f85-427a-8257-10f5d38452f7
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_category::operator==
Tests for equality between `error_category` objects.  
  
## Syntax  
  
```  
bool operator==(const error_category& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The object to be tested for equality.|  
  
## Return Value  
 **true** if the objects are equal; **false** if the objects are not equal.  
  
## Remarks  
 This member operator returns `this == &_Right`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)