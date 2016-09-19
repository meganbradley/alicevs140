---
title: "Event::operator= Operator"
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
ms.topic: reference
ms.assetid: d8fe9820-8856-4899-9553-56226bdc4945
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event::operator= Operator
Assigns the specified Event reference to the current Event instance.  
  
## Syntax  
  
```  
WRL_NOTHROW Event& operator=(  
   _Inout_ Event&& h  
);  
```  
  
#### Parameters  
 `h`  
 An rvalue-reference to an Event instance.  
  
## Return Value  
 A pointer to the current Event instance.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Event Class](../vs140/Event-Class--Windows-Runtime-C---Template-Library-.md)