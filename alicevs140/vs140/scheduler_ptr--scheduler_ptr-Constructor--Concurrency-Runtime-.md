---
title: "scheduler_ptr::scheduler_ptr Constructor (Concurrency Runtime)"
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
ms.assetid: 526f1c08-363f-4963-b7d6-2d5ffea1939a
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# scheduler_ptr::scheduler_ptr Constructor (Concurrency Runtime)
Creates a scheduler pointer from shared_ptr to scheduler  
  
## Syntax  
  
```  
explicit scheduler_ptr(  
   std::shared_ptr<scheduler_interface> scheduler  
);  
  
explicit scheduler_ptr(  
   _In_opt_ scheduler_interface * pScheduler  
);  
```  
  
#### Parameters  
 `scheduler`  
 `pScheduler`  
  
## Requirements  
 **Header:** pplinterface.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [scheduler_ptr Structure (Concurrency Runtime)](../vs140/scheduler_ptr-Structure--Concurrency-Runtime-.md)