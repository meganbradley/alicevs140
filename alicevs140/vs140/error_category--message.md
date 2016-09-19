---
title: "error_category::message"
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
ms.assetid: 9e630ae4-23d3-4f9c-97ed-43a11221d459
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_category::message
Returns the name of the specified error code.  
  
## Syntax  
  
```  
virtual string message(error_code::value_type _Val) const = 0;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Val`|The error code value to describe.|  
  
## Return Value  
 Returns a descriptive name of the error code `_Val` for the category.  
  
## Remarks  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)