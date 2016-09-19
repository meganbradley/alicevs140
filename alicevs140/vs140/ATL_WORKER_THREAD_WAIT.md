---
title: "ATL_WORKER_THREAD_WAIT"
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
ms.assetid: 4d209004-47f4-4c6a-98b4-aee49ffb0911
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL_WORKER_THREAD_WAIT
This macro defines the default value in milliseconds that [CWorkerThread::Shutdown](../vs140/CWorkerThread--Shutdown.md) will wait for the worker thread to shut down.  
  
## Syntax  
  
```  
  
#define ATL_WORKER_THREAD_WAIT  
  
```  
  
## Remarks  
 ATL_WORKER_THREAD_WAIT defaults to 10 seconds. If necessary, you can define your own value for this symbol before including atlutil.h.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)