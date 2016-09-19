---
title: "bad_target::bad_target Constructor"
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
ms.assetid: 12b4df2a-3837-44c0-b6e2-bf988ce73a17
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bad_target::bad_target Constructor
Constructs a `bad_target` object.  
  
## Syntax  
  
```  
explicit _CRTIMP bad_target(  
   _In_z_ const char * _Message  
) throw();  
  
bad_target() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [bad_target Class](../vs140/bad_target-Class.md)