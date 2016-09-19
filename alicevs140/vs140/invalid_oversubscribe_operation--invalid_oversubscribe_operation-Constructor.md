---
title: "invalid_oversubscribe_operation::invalid_oversubscribe_operation Constructor"
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
ms.assetid: c9ff9030-4a20-482c-8b5c-223100157a52
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_oversubscribe_operation::invalid_oversubscribe_operation Constructor
Constructs an `invalid_oversubscribe_operation` object.  
  
## Syntax  
  
```  
explicit _CRTIMP invalid_oversubscribe_operation(  
   _In_z_ const char * _Message  
) throw();  
  
invalid_oversubscribe_operation() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [invalid_oversubscribe_operation Class](../vs140/invalid_oversubscribe_operation-Class.md)