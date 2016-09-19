---
title: "scheduler_worker_creation_error::scheduler_worker_creation_error Constructor"
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
ms.assetid: f30f3931-18e5-4985-abe2-a9c1a42a718b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scheduler_worker_creation_error::scheduler_worker_creation_error Constructor
Constructs a `scheduler_worker_creation_error` object.  
  
## Syntax  
  
```  
scheduler_worker_creation_error(  
   _In_z_ const char * _Message,  
   HRESULT _Hresult  
) throw();  
  
explicit _CRTIMP scheduler_worker_creation_error(  
   HRESULT _Hresult  
) throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
 `_Hresult`  
 The `HRESULT` value of the error that caused the exception.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [scheduler_worker_creation_error Class](../vs140/scheduler_worker_creation_error-Class.md)