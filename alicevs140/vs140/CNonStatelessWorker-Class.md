---
title: "CNonStatelessWorker Class"
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
ms.assetid: d00936c6-9e7d-49fb-b87d-417b963367d1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNonStatelessWorker Class
Receives requests from a thread pool and passes them on to a worker object that is created and destroyed on each request.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template <  
   class  Worker>  
   class CNonStatelessWorker  
  
```  
  
#### Parameters  
 *Worker*  
 A worker thread class conforming to the [worker archetype](../vs140/Worker-Archetype.md) suitable for handling requests queued on [CThreadPool](../vs140/CThreadPool-Class.md).  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CNonStatelessWorker::RequestType](../vs140/CNonStatelessWorker--RequestType.md)|Implementation of [WorkerArchetype::RequestType](../vs140/WorkerArchetype--RequestType.md).|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CNonStatelessWorker::Execute](../vs140/CNonStatelessWorker--Execute.md)|Implementation of [WorkerArchetype::Execute](../vs140/WorkerArchetype--Execute.md).|  
|[CNonStatelessWorker::Initialize](../vs140/CNonStatelessWorker--Initialize.md)|Implementation of [WorkerArchetype::Initialize](../vs140/WorkerArchetype--Initialize.md).|  
|[CNonStatelessWorker::Terminate](../vs140/CNonStatelessWorker--Terminate.md)|Implementation of [WorkerArchetype::Terminate](../vs140/WorkerArchetype--Terminate.md).|  
  
## Remarks  
 This class is a simple worker thread for use with [CThreadPool](../vs140/CThreadPool-Class.md). This class doesn't provide any request-handling capabilities of its own. Instead, it instantiates one instance of *Worker* per request and delegates the implementation of its methods to that instance.  
  
 The benefit of this class is that it provides a convenient way to change the state model for existing worker thread classes. `CThreadPool` will create a single worker for the lifetime of the thread, so if the worker class holds state, it will hold it across multiple requests. By simply wrapping that class in the `CNonStatelessWorker` template before using it with `CThreadPool`, the lifetime of the worker and the state it holds is limited to a single request.  
  
## Requirements  
 **Header:** atlutil.h  
  
##  <a name="cnonstatelessworker__execute"></a>  CNonStatelessWorker::Execute  
 Implementation of [WorkerArchetype::Execute](../vs140/WorkerArchetype--Execute.md).  
  
```  
  
void Execute(  
      Worker::RequestType  request,  
      void*  pvWorkerParam,  
      OVERLAPPED*  pOverlapped  
   );  
  
```  
  
### Remarks  
 This method creates an instance of the *Worker* class on the stack and calls [Initialize](../vs140/WorkerArchetype--Initialize.md) on that object. If the initialization is successful, this method also calls [Execute](../vs140/WorkerArchetype--Execute.md) and [Terminate](../vs140/WorkerArchetype--Terminate.md) on the same object.  
  
##  <a name="cnonstatelessworker__initialize"></a>  CNonStatelessWorker::Initialize  
 Implementation of [WorkerArchetype::Initialize](../vs140/WorkerArchetype--Initialize.md).  
  
```  
  
BOOL Initialize(  
      void* /* pvParam  
   */  
   ) throw( );  
  
```  
  
### Return Value  
 Always returns TRUE.  
  
### Remarks  
 This class does not do any initialization in `Initialize`.  
  
##  <a name="cnonstatelessworker__requesttype"></a>  CNonStatelessWorker::RequestType  
 Implementation of [WorkerArchetype::RequestType](../vs140/WorkerArchetype--RequestType.md).  
  
```  
  
typedef Worker::RequestType RequestType;  
  
```  
  
### Remarks  
 This class handles the same type of work item as the class used for the *Worker* template parameter. See [CNonStatelessWorker Overview](../vs140/CNonStatelessWorker-Class.md) for details.  
  
##  <a name="cnonstatelessworker__terminate"></a>  CNonStatelessWorker::Terminate  
 Implementation of [WorkerArchetype::Terminate](../vs140/WorkerArchetype--Terminate.md).  
  
```  
  
void Terminate(  
      void* /* pvParam  
   */  
   ) throw( );  
  
```  
  
### Remarks  
 This class does not do any cleanup in `Terminate`.  
  
## See Also  
 [CThreadPool Class](../vs140/CThreadPool-Class.md)   
 [Worker Archetype](../vs140/Worker-Archetype.md)   
 [ATL Classes](../vs140/ATL-Classes.md)