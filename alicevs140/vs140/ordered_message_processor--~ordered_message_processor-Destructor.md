---
title: "ordered_message_processor::~ordered_message_processor Destructor"
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
ms.assetid: e1b432ba-41ef-4212-a60c-98409f78a34e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ordered_message_processor::~ordered_message_processor Destructor
Destroys the `ordered_message_processor` object.  
  
## Syntax  
  
```  
virtual ~ordered_message_processor();  
```  
  
## Remarks  
 Waits for all outstanding asynchronous operations before destroying the processor.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ordered_message_processor Class](../vs140/ordered_message_processor-Class.md)