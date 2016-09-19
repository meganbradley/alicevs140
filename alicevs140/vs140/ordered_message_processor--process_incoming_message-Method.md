---
title: "ordered_message_processor::process_incoming_message Method"
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
ms.assetid: d5dcf035-0dd5-48fa-a678-ec2631fa2380
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ordered_message_processor::process_incoming_message Method
The processing function that is called asynchronously. It dequeues messages and begins processing them.  
  
## Syntax  
  
```  
virtual void process_incoming_message();  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ordered_message_processor Class](../vs140/ordered_message_processor-Class.md)