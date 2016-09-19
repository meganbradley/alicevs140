---
title: "task_canceled::task_canceled Constructor"
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
ms.assetid: cba7b785-efe9-4e4a-8994-ce30323dbf9e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task_canceled::task_canceled Constructor
Constructs a `task_canceled` object.  
  
## Syntax  
  
```  
explicit _CRTIMP task_canceled(  
   _In_z_ const char * _Message  
) throw();  
  
task_canceled() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task_canceled Class](../vs140/task_canceled-Class.md)