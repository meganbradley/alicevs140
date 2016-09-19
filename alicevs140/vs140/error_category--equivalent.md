---
title: "error_category::equivalent"
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
ms.assetid: d86769b3-a9ea-45a0-8cfc-5bf79c4b95f5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# error_category::equivalent
Returns a value that specifies whether error objects are equivalent.  
  
## Syntax  
  
```  
virtual bool equivalent(value_type _Errval,  
    const error_condition& _Cond) const;  
virtual bool equivalent(const error_code& _Code,  
    value_type _Errval) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errval`|The error code value to compare.|  
|`_Cond`|The [error_condition](../vs140/error_condition-Class.md) object to compare.|  
|`_Code`|The [error_code](../vs140/error_code-Class.md) object to compare.|  
  
## Return Value  
 `true` if the category and value are equal; otherwise, `false`.  
  
## Remarks  
 The first member function returns `*this == _Cond.category() && _Cond.value() == _Errval`.  
  
 The second member function returns `*this == _Code.category() && _Code.value() == _Errval`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [error_category Class](../vs140/error_category-Class.md)