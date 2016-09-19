---
title: "propagator_block::decline_incoming_messages Method"
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
ms.assetid: 248011c5-c197-4e86-b4d4-354e00048a7f
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# propagator_block::decline_incoming_messages Method
Indicates to the block that new messages should be declined.  
  
## Syntax  
  
```  
void decline_incoming_messages();  
```  
  
## Remarks  
 This method is called by the destructor to ensure that new messages are declined while destruction is in progress.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [propagator_block Class](../vs140/propagator_block-Class.md)