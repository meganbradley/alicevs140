---
title: "error_category::operator&lt;"
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
ms.assetid: d69ab9ca-7f85-4d9c-a066-f188aec9c59c
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_category::operator&lt;
Tests if the [error_category](../vs140/error_category-Class.md) object is less than the `error_category` object passed in for comparison.  
  
## Syntax  
  
```  
bool operator<(const error_category& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The `error_category` object to be compared.|  
  
## Return Value  
 **true** if the `error_category` object is less than the `error_category` object passed in for comparison; Otherwise, **false**.  
  
## Remarks  
 The member operator returns `this < &_Right`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)