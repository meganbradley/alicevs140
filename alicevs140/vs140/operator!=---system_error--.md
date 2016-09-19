---
title: "operator!= (&lt;system_error&gt;)"
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
ms.assetid: cdb46cb5-f081-46e7-8e89-77c7e545e26f
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# operator!= (&lt;system_error&gt;)
Tests if the object on the left side of the operator is not equal to the object on the right side.  
  
## Syntax  
  
```  
bool operator!=(const error_code& _Left, const error_condition& _Right);  
bool operator!=(const error_condition& _Left, const error_code& _Right);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Left`|The object to be tested for inequality.|  
|`_Right`|The object to be tested for inequality.|  
  
## Return Value  
 **true** if the object passed in `_Left` is not equal to the object passed in `_Right`; otherwise **false**.  
  
## Remarks  
 This function returns `!(_Left == _Right)`.  
  
## See Also  
 [<system_error>](../vs140/-system_error-.md)