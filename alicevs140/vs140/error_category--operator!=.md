---
title: "error_category::operator!="
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
ms.assetid: acf40736-d113-42a2-97e1-736a53ab98db
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_category::operator!=
Tests for inequality between `error_category` objects.  
  
## Syntax  
  
```  
bool operator!=(const error_category& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The object to be tested for inequality.|  
  
## Return Value  
 **true** if the `error_category` object is not equal to the `error_category` object passed in `_Right`; otherwise **false**.  
  
## Remarks  
 The member operator returns `(!*this == _Right)`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)