---
title: "structured_task_group::~structured_task_group Destructor"
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
ms.assetid: 79f4df3d-3bab-4599-b8bd-2530e47a1d09
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# structured_task_group::~structured_task_group Destructor
Destroys a `structured_task_group` object. You are expected to call either the `wait` or `run_and_wait` method on the object prior to the destructor executing, unless the destructor is executing as a result of stack unwinding due to an exception.  
  
## Syntax  
  
```  
~structured_task_group();  
```  
  
## Remarks  
 If the destructor runs as the result of normal execution (for example, not stack unwinding due to an exception) and neither the `wait` nor `run_and_wait` methods have been called, the destructor may throw a [missing_wait](../vs140/missing_wait-Class.md) exception.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [structured_task_group Class](../vs140/structured_task_group-Class.md)   
 [structured_task_group::wait Method](../vs140/structured_task_group--wait-Method.md)   
 [structured_task_group::run_and_wait Method](../vs140/structured_task_group--run_and_wait-Method.md)