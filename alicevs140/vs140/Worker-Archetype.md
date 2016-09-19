---
title: "Worker Archetype"
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
ms.assetid: 834145cd-09d3-4149-bc99-620e1871cbfb
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Worker Archetype
Classes that conform to the *worker* archetype provide the code to process work items queued on a thread pool.  
  
 **Implementation**  
  
 To implement a class conforming to this archetype, the class must provide the following features:  
  
|Method|Description|  
|------------|-----------------|  
|[Initialize](../vs140/WorkerArchetype--Initialize.md)|Called to initialize the worker object before any requests are passed to [Execute](../vs140/WorkerArchetype--Execute.md).|  
|[Execute](../vs140/WorkerArchetype--Execute.md)|Called to process a work item.|  
|[Terminate](../vs140/WorkerArchetype--Terminate.md)|Called to uninitialize the worker object after all requests have been passed to [Execute](../vs140/WorkerArchetype--Execute.md).|  
  
|Typedef|Description|  
|-------------|-----------------|  
|[RequestType](../vs140/WorkerArchetype--RequestType.md)|A typedef for the type of work item that can be processed by the worker class.|  
  
 A typical *worker* class looks like this:  
  
 [!CODE [NVC_ATL_Utilities#137](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#137)]  
  
 **Existing Implementations**  
  
 These classes conform to this archetype:  
  
|Class|Description|  
|-----------|-----------------|  
|[CNonStatelessWorker](../vs140/CNonStatelessWorker-Class.md)|Receives requests from the thread pool and passes them on to a worker object that is created and destroyed for each request.|  
  
 **Use**  
  
 These template parameters expect the class to conform to this archetype:  
  
|Parameter name|Used by|  
|--------------------|-------------|  
|*Worker*|[CThreadPool](../vs140/CThreadPool-Class.md)|  
|*Worker*|[CNonStatelessWorker](../vs140/CNonStatelessWorker-Class.md)|  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Archetypes](../vs140/ATL-Archetypes.md)   
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)