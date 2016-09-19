---
title: "improper_scheduler_reference::improper_scheduler_reference Constructor"
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
ms.assetid: a6c02ce9-b8b7-468a-982d-41e55417a0cd
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# improper_scheduler_reference::improper_scheduler_reference Constructor
Constructs an `improper_scheduler_reference` object.  
  
## Syntax  
  
```  
explicit _CRTIMP improper_scheduler_reference(  
   _In_z_ const char* _Message  
) throw();  
  
improper_scheduler_reference() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [improper_scheduler_reference Class](../vs140/improper_scheduler_reference-Class.md)