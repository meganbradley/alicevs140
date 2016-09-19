---
title: "unbounded_buffer::propagate_output_messages Method"
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
ms.assetid: b4151a7e-105d-4761-a542-aaf641c527d5
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unbounded_buffer::propagate_output_messages Method
Places the `message``_PMessage` in this `unbounded_buffer` messaging block and tries to offer it to all of the linked targets.  
  
## Syntax  
  
```  
virtual void propagate_output_messages();  
```  
  
## Remarks  
 If another message is already ahead of this one in the `unbounded_buffer`, propagation to linked targets will not occur until any earlier messages have been accepted or consumed. The first linked target to successfully `accept` or `consume` the message takes ownership, and no other target can then get the message.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [unbounded_buffer Class](../vs140/unbounded_buffer-Class.md)