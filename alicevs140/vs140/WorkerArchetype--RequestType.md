---
title: "WorkerArchetype::RequestType"
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
ms.topic: reference
ms.assetid: 22a4a478-9cbe-4230-b0b7-0f85ecb219dc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WorkerArchetype::RequestType
A typedef for the type of work item that can be processed by the worker class.  
  
## Syntax  
  
```  
  
typedef   
MyRequestType  
 RequestType;  
  
```  
  
## Remarks  
 This type must be used as the first parameter of [Execute](../vs140/WorkerArchetype--Execute.md) and must be capable of being cast to and from a ULONG_PTR.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [Worker Archetype](../vs140/Worker-Archetype.md)