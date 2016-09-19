---
title: "task::is_apartment_aware Method"
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
ms.assetid: 729fa9b7-6af3-45ad-94b6-ab205d9be1d2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task::is_apartment_aware Method
Determines whether the task unwraps a Windows Runtime `IAsyncInfo` interface or is descended from such a task.  
  
## Syntax  
  
```  
bool is_apartment_aware() const;  
```  
  
## Return Value  
 `true` if the task unwraps an `IAsyncInfo` interface or is descended from such a task, `false` otherwise.  
  
## Requirements  
 **Header:** ppltasks.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task Class (Concurrency Runtime)](../vs140/task-Class--Concurrency-Runtime-.md)