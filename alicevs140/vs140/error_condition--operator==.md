---
title: "error_condition::operator=="
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 384d46a3-c6b6-4539-956a-3985e1b79249
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_condition::operator==
Tests for equality between `error_condition` objects.  
  
## Syntax  
  
```  
bool operator==(const error_condition& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The ojbect to be tested for equality.|  
  
## Return Value  
 **true** if the objects are equal; **false** if objects are not equal.  
  
## Remarks  
 The member operator returns `category() == _Right.category() && value == _Right.value()`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_condition Class](../vs140/error_condition-Class.md)