---
title: "join::propagate_to_any_targets Method"
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
ms.assetid: ad3f4de7-7013-4527-935a-f494c76d7f0f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# join::propagate_to_any_targets Method
Constructs an output message containing an input message from each source when they have all propagated a message. Sends this output message out to each of its targets.  
  
## Syntax  
  
```  
void propagate_to_any_targets(  
   _Inout_opt_ message<_OutputType> *  
);  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [join Class](../vs140/join-Class.md)