---
title: "scheduler_resource_allocation_error::get_error_code Method"
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
ms.assetid: 88cca0c7-cacc-4326-95c5-4d9868170159
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scheduler_resource_allocation_error::get_error_code Method
Returns the error code that caused the exception.  
  
## Syntax  
  
```  
HRESULT get_error_code() const throw();  
```  
  
## Return Value  
 The `HRESULT` value of the error that caused the exception.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [scheduler_resource_allocation_error Class](../vs140/scheduler_resource_allocation_error-Class.md)