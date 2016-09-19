---
title: "error_condition::operator!="
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
ms.assetid: 6bcebe28-2667-4cd8-839b-6b6fc67aa187
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_condition::operator!=
Tests for inequality between `error_condition` objects.  
  
## Syntax  
  
```  
bool operator!=(const error_condition& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The object to be tested for inequality.|  
  
## Return Value  
 **true** if the `error_condition` object is not equal to the `error_condition` object passed in `_Right`; otherwise **false**.  
  
## Remarks  
 The member operator returns `!(*this == _Right)`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_condition Class](../vs140/error_condition-Class.md)