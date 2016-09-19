---
title: "GetSchedulerId Function"
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
ms.assetid: 30b63059-9712-43d2-8958-443489282c7a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetSchedulerId Function
Returns a unique identifier that can be assigned to a scheduler that implements the `IScheduler` interface.  
  
## Syntax  
  
```  
unsigned int __cdecl GetSchedulerId();  
```  
  
## Return Value  
 A unique identifier for a scheduler.  
  
## Remarks  
 Use this method to obtain an identifier for your scheduler before you pass an `IScheduler` interface as a parameter to any of the methods offered by the Resource Manager.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)