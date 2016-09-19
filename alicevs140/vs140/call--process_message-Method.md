---
title: "call::process_message Method"
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
ms.assetid: b4ef4cb4-52f3-4e88-86dd-5e37e077970e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# call::process_message Method
Processes a message that was accepted by this `call` messaging block.  
  
## Syntax  
  
```  
virtual void process_message(  
   _Inout_ message<_Type> * _PMessage  
);  
```  
  
#### Parameters  
 `_PMessage`  
 A pointer to the message that is to be handled.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [call Class](../vs140/call-Class.md)