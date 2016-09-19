---
title: "invalid_multiple_scheduling::invalid_multiple_scheduling Constructor"
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
ms.assetid: 12584bbb-7293-44fb-a7e9-d656966937c3
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_multiple_scheduling::invalid_multiple_scheduling Constructor
Constructs an `invalid_multiple_scheduling` object.  
  
## Syntax  
  
```  
explicit _CRTIMP invalid_multiple_scheduling(  
   _In_z_ const char * _Message  
) throw();  
  
invalid_multiple_scheduling() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [invalid_multiple_scheduling Class](../vs140/invalid_multiple_scheduling-Class.md)