---
title: "error_code::operator&lt;"
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
ms.assetid: af3b205a-3376-40d4-a331-365d03cfc918
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_code::operator&lt;
Tests if the [error_code](assetId:///09c6ef90-b6f8-430a-b584-e168716c7e31) object is less than the `error_code` object passed in for comparison.  
  
## Syntax  
  
```  
bool operator<(const error_code& _Right) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|The error_code object to be compared.|  
  
## Return Value  
 **true** if the `error_code` object is less than the `error_code` object passed in for comparison; Otherwise, **false**.  
  
## Remarks  
 The member operator returns `category() < _Right.category() || category() == _Right.category() && value < _Right.value()`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_code Class](../vs140/error_code-Class.md)