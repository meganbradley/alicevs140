---
title: "make_error_code"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 08e4c052-a013-4f9b-a82f-4f8b18e8f7fa
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# make_error_code
Creates an error code object.  
  
## Syntax  
  
```  
error_code make_error_code(generic_errno _Errno);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Errno`|The enumeration value to store in the error code object.|  
  
## Return Value  
 The error code object.  
  
## Remarks  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [<system_error>](../vs140/-system_error-.md)