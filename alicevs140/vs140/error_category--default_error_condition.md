---
title: "error_category::default_error_condition"
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
ms.assetid: 69114c5c-a3ff-4668-b39b-073d8cea9e2a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_category::default_error_condition
Stores the error code value for an error condition object.  
  
## Syntax  
  
```  
virtual error_condition default_error_condition(int _Errval) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errval`|The error code value to store in the [error_condition](../vs140/error_condition-Class.md).|  
  
## Return Value  
 Returns `error_condition(_Errval, *this)`.  
  
## Remarks  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)