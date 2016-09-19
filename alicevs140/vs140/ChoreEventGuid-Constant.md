---
title: "ChoreEventGuid Constant"
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
ms.assetid: 1c0ec298-ce70-41b1-9458-6384c0bbf45e
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ChoreEventGuid Constant
A category GUID describing ETW events fired by the Concurrency Runtime that are directly related to chores or tasks.  
  
## Syntax  
  
```  
const __declspec(selectany) GUID ChoreEventGuid = { 0x7E854EC7, 0xCDC4, 0x405a, { 0xB5, 0xB2, 0xAA, 0xF7, 0xC9, 0xE7, 0xD4, 0x0C } };  
```  
  
## Remarks  
 This category of events is not currently fired by the Concurrency Runtime.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [task_group Class](../vs140/task_group-Class.md)   
 [structured_task_group Class](../vs140/structured_task_group-Class.md)