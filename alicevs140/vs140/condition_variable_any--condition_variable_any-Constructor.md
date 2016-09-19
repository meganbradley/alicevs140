---
title: "condition_variable_any::condition_variable_any Constructor"
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
ms.assetid: d5894374-bd5b-48cf-96f5-e266ece47a09
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# condition_variable_any::condition_variable_any Constructor
Constructs a `condition_variable_any` object.  
  
## Syntax  
  
```  
condition_variable_any();  
```  
  
## Remarks  
 If not enough memory is available, the constructor throws a [system_error](../vs140/system_error-Class.md) object that has a `not_enough_memory` error code. If the object cannot be constructed because some other resource is not available, the constructor throws a `system_error` object that has a `resource_unavailable_try_again` error code.  
  
## Requirements  
 **Header:** condition_variable  
  
 **Namespace:** std  
  
## See Also  
 [condition_variable_any Class](../vs140/condition_variable_any-Class.md)   
 [<condition_variable>](../vs140/-condition_variable-.md)