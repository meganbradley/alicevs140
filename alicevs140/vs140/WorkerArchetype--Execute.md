---
title: "WorkerArchetype::Execute"
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
ms.assetid: f5d1de03-b034-4d54-898f-cbdedd68e04d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WorkerArchetype::Execute
Called to process a work item.  
  
## Syntax  
  
```  
  
      void Execute(  
   RequestType request,  
   void* pvWorkerParam,  
   OVERLAPPED* pOverlapped   
);  
```  
  
#### Parameters  
 `request`  
 The work item to be processed. The work item is of the same type as [RequestType](../vs140/WorkerArchetype--RequestType.md).  
  
 `pvWorkerParam`  
 A custom parameter understood by the worker class. Also passed to [Initialize](../vs140/WorkerArchetype--Initialize.md) and [Terminate](../vs140/WorkerArchetype--Terminate.md).  
  
 `pOverlapped`  
 A pointer to the [OVERLAPPED](http://msdn.microsoft.com/library/windows/desktop/ms684342) structure used to create the queue on which work items were queued.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [Worker Archetype](../vs140/Worker-Archetype.md)