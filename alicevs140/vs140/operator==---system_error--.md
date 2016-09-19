---
title: "operator== (&lt;system_error&gt;)"
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
ms.assetid: 7bd6bee0-8044-4674-9993-5c9f07553d9a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator== (&lt;system_error&gt;)
Tests if the object on the left side of the operator is equal to the object on the right side.  
  
## Syntax  
  
```  
bool operator==(const error_code& _Left, const error_condition& _Right);  
bool operator==(const error_condition& _Left, const error_code& _Right);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Left`|The object to be tested for equality.|  
|`_Right`|The object to be tested for equality.|  
  
## Return Value  
 **true** if the objects are equal; **false** if objects are not equal.  
  
## Remarks  
 This function returns `_Left.category() == _Right.category() && _Left.value() == _Right.value()`.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [<system_error>](../vs140/-system_error-.md)