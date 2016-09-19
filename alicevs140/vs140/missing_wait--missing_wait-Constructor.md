---
title: "missing_wait::missing_wait Constructor"
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
ms.assetid: 8d0128ef-2dd8-42f3-9716-bc3e12a3c704
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# missing_wait::missing_wait Constructor
Constructs a `missing_wait` object.  
  
## Syntax  
  
```  
explicit _CRTIMP missing_wait(  
   _In_z_ const char * _Message  
) throw();  
  
missing_wait() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [missing_wait Class](../vs140/missing_wait-Class.md)