---
title: "CNonStatelessWorker::Execute"
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
ms.assetid: a8205d96-087f-4813-97ff-5ac783d9c259
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNonStatelessWorker::Execute
Implementation of [WorkerArchetype::Execute](../vs140/WorkerArchetype--Execute.md).  
  
## Syntax  
  
```  
  
      void Execute(  
   Worker::RequestType request,  
   void* pvWorkerParam,  
   OVERLAPPED* pOverlapped   
);  
```  
  
## Remarks  
 This method creates an instance of the *Worker* class on the stack and calls [Initialize](../vs140/WorkerArchetype--Initialize.md) on that object. If the initialization is successful, this method also calls [Execute](../vs140/WorkerArchetype--Execute.md) and [Terminate](../vs140/WorkerArchetype--Terminate.md) on the same object.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CNonStatelessWorker Class](../vs140/CNonStatelessWorker-Class.md)