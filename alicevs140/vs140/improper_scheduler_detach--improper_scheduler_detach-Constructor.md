---
title: "improper_scheduler_detach::improper_scheduler_detach Constructor"
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
ms.assetid: 5072e1b0-61d2-41c0-b7f4-3ad39e18a42f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# improper_scheduler_detach::improper_scheduler_detach Constructor
Constructs an `improper_scheduler_detach` object.  
  
## Syntax  
  
```  
explicit _CRTIMP improper_scheduler_detach(  
   _In_z_ const char * _Message  
) throw();  
  
improper_scheduler_detach() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [improper_scheduler_detach Class](../vs140/improper_scheduler_detach-Class.md)