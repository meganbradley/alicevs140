---
title: "CNonStatelessWorker::Terminate"
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
ms.assetid: 0e1a6c79-f759-49e9-8ee2-4328629f1962
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNonStatelessWorker::Terminate
Implementation of [WorkerArchetype::Terminate](../vs140/WorkerArchetype--Terminate.md).  
  
## Syntax  
  
```  
  
      void Terminate(  
   void* /*pvParam*/  
) throw( );  
```  
  
## Remarks  
 This class does not do any cleanup in `Terminate`.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CNonStatelessWorker Class](../vs140/CNonStatelessWorker-Class.md)