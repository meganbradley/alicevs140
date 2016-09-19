---
title: "operation_timed_out::operation_timed_out Constructor"
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
ms.assetid: 4305805c-44c6-4355-bb8a-0f41faeea104
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operation_timed_out::operation_timed_out Constructor
Constructs an `operation_timed_out` object.  
  
## Syntax  
  
```  
explicit _CRTIMP operation_timed_out(  
   _In_z_ const char * _Message  
) throw();  
  
operation_timed_out() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [operation_timed_out Class](../vs140/operation_timed_out-Class.md)