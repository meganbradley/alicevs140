---
title: "ordered_message_processor::wait Method"
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
ms.assetid: 6b982ff8-93db-4406-b1f0-2c22bb882d9f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ordered_message_processor::wait Method
A processor-specific spin wait used in destructors of message blocks to make sure that all asynchronous processing tasks have time to finish before destroying the block.  
  
## Syntax  
  
```  
virtual void wait();  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ordered_message_processor Class](../vs140/ordered_message_processor-Class.md)