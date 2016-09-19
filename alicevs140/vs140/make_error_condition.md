---
title: "make_error_condition"
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
ms.assetid: 97d0e27e-7f61-448e-983b-331f8b9d6c21
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# make_error_condition
Creates an error condition object.  
  
## Syntax  
  
```  
error_condition make_error_condition(generic_errno _Errno);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errno`|The enumeration value to store in the error condition object.|  
  
## Return Value  
 The error condition object.  
  
## Remarks  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [<system_error>](../vs140/-system_error-.md)