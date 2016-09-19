---
title: "error_condition::operator&lt;"
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
ms.assetid: 69c8a76a-7098-47db-b276-71765b3c7d3a
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_condition::operator&lt;
Tests if the `error_condition` object is less than the `error_code` object passed in for comparison.  
  
## Syntax  
  
```  
bool operator<(const error_condition& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The `error_condition` object to be compared.|  
  
## Return Value  
 **true** if the `error_condition` object is less than the `error_condition` object passed in for comparison; Otherwise, **false**.  
  
## Remarks  
 The member operator returns `category() < _Right.category() || category() == _Right.category() && value < _Right.value()`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_condition Class](../vs140/error_condition-Class.md)