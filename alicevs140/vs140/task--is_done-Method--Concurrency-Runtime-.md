---
title: "task::is_done Method (Concurrency Runtime)"
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
ms.assetid: 1fa97965-c198-4946-81fa-af7124fd0c22
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task::is_done Method (Concurrency Runtime)
Determines if the task is completed.  
  
## Syntax  
  
```  
bool is_done() const;  
```  
  
## Return Value  
 True if the task has completed, false otherwise.  
  
## Remarks  
 The function returns true if the task is completed or canceled (with or without user exception).  
  
## Requirements  
 **Header:** ppltasks.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task Class (Concurrency Runtime)](../vs140/task-Class--Concurrency-Runtime-.md)