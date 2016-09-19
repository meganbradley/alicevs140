---
title: "WorkerArchetype::Initialize"
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
ms.assetid: 5d82463f-dba9-461c-bc8d-692ff15ed17e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WorkerArchetype::Initialize
Called to initialize the worker object before any requests are passed to [Execute](../vs140/WorkerArchetype--Execute.md).  
  
## Syntax  
  
```  
  
      BOOL Initialize(  
   void* pvParam  
) throw( );  
```  
  
#### Parameters  
 `pvParam`  
 A custom parameter understood by the worker class. Also passed to [Terminate](../vs140/WorkerArchetype--Terminate.md) and [Execute](../vs140/WorkerArchetype--Execute.md).  
  
## Return Value  
 Return **TRUE** on success, **FALSE** on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [Worker Archetype](../vs140/Worker-Archetype.md)