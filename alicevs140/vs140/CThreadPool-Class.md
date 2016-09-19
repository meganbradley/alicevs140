---
title: "CThreadPool Class"
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
ms.assetid: 06683718-01b9-413c-9481-2dc1734ec70f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CThreadPool Class
This class provides a pool of worker threads that process a queue of work items.  
  
## Syntax  
  
```  
  
template <class Worker,  
      class  ThreadTraits  
    = DefaultThreadTraits>  
   class CThreadPool :  
      public IThreadPoolConfig  
  
```  
  
#### Parameters  
 *Worker*  
 The class conforming to the [worker archetype](../vs140/Worker-Archetype.md) providing the code used to process work items queued on the thread pool.  
  
 `ThreadTraits`  
 The class providing the function used to create the threads in the pool.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CThreadPool::CThreadPool](../vs140/CThreadPool--CThreadPool.md)|The constructor for the thread pool.|  
|[CThreadPool::~CThreadPool](../vs140/CThreadPool--~CThreadPool.md)|The destructor for the thread pool.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CThreadPool::AddRef](../vs140/CThreadPool--AddRef.md)|Implementation of `IUnknown::AddRef`.|  
|[CThreadPool::GetNumThreads](../vs140/CThreadPool--GetNumThreads.md)|Call this method to get the number of threads in the pool.|  
|[CThreadPool::GetQueueHandle](../vs140/CThreadPool--GetQueueHandle.md)|Call this method to get the handle of the IO completion port used to queue work items.|  
|[CThreadPool::GetSize](../vs140/CThreadPool--GetSize.md)|Call this method to get the number of threads in the pool.|  
|[CThreadPool::GetTimeout](../vs140/CThreadPool--GetTimeout.md)|Call this method to get the maximum time in milliseconds that the thread pool will wait for a thread to shut down.|  
|[CThreadPool::Initialize](../vs140/CThreadPool--Initialize.md)|Call this method to initialize the thread pool.|  
|[CThreadPool::QueryInterface](../vs140/CThreadPool--QueryInterface.md)|Implementation of **IUnknown::QueryInterface**.|  
|[CThreadPool::QueueRequest](../vs140/CThreadPool--QueueRequest.md)|Call this method to queue a work item to be handled by a thread in the pool.|  
|[CThreadPool::Release](../vs140/CThreadPool--Release.md)|Implementation of `IUnknown::Release`.|  
|[CThreadPool::SetSize](../vs140/CThreadPool--SetSize.md)|Call this method to set the number of threads in the pool.|  
|[CThreadPool::SetTimeout](../vs140/CThreadPool--SetTimeout.md)|Call this method to set the maximum time in milliseconds that the thread pool will wait for a thread to shut down.|  
|[CThreadPool::Shutdown](../vs140/CThreadPool--Shutdown.md)|Call this method to shut down the thread pool.|  
  
## Remarks  
 Threads in the pool are created and destroyed when the pool is initialized, resized, or shut down. An instance of class *Worker* will be created on the stack of each worker thread in the pool. Each instance will live for the lifetime of the thread.  
  
 Immediately after creation of a thread, *Worker*:: `Initialize` will be called on the object associated with that thread. Immediately before destruction of a thread, *Worker*:: `Terminate` will be called. Both methods must accept a **void\*** argument. The value of this argument is passed to the thread pool through the `pvWorkerParam` parameter of [CThreadPool::Initialize](../vs140/CThreadPool--Initialize.md).  
  
 When there are work items in the queue and worker threads available for work, a worker thread will pull an item off the queue and call the **Execute** method of the *Worker* object for that thread. Three items are then passed to the method: the item from the queue, the same `pvWorkerParam` passed to *Worker*:: `Initialize` and *Worker*:: `Terminate`, and a pointer to the [OVERLAPPED](http://msdn.microsoft.com/library/windows/desktop/ms684342) structure used for the IO completion port queue.  
  
 The *Worker* class declares the type of the items that will be queued on the thread pool by providing a typedef, *Worker*:: `RequestType`. This type must be capable of being cast to and from a **ULONG_PTR**.  
  
 An example of a *Worker* class is [CNonStatelessWorker Class](../vs140/CNonStatelessWorker-Class.md).  
  
## Inheritance Hierarchy  
 `IUnknown`  
  
 [IThreadPoolConfig](../vs140/IThreadPoolConfig-Interface.md)  
  
 `CThreadPool`  
  
## Requirements  
 **Header:** atlutil.h  
  
##  <a name="cthreadpool__addref"></a>  CThreadPool::AddRef  
 Implementation of `IUnknown::AddRef`.  
  
```  
  
ULONG STDMETHODCALLTYPE AddRef( ) throw( );  
  
```  
  
### Return Value  
 Always returns 1.  
  
### Remarks  
 This class does not implement lifetime control using reference counting.  
  
##  <a name="cthreadpool__cthreadpool"></a>  CThreadPool::CThreadPool  
 The constructor for the thread pool.  
  
```  
  
CThreadPool( ) throw( );  
  
```  
  
### Remarks  
 Initializes the timeout value to [ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT](../vs140/ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT.md).  
  
##  <a name="cthreadpool___dtorcthreadpool"></a>  CThreadPool::~CThreadPool  
 The destructor for the thread pool.  
  
```  
  
~CThreadPool( ) throw( );  
  
```  
  
### Remarks  
 Calls [CThreadPool::Shutdown](../vs140/CThreadPool--Shutdown.md).  
  
##  <a name="cthreadpool__getnumthreads"></a>  CThreadPool::GetNumThreads  
 Call this method to get the number of threads in the pool.  
  
```  
  
int GetNumThreads( ) throw( );  
  
```  
  
### Return Value  
 Returns the number of threads in the pool.  
  
##  <a name="cthreadpool__getqueuehandle"></a>  CThreadPool::GetQueueHandle  
 Call this method to get the handle of the IO completion port used to queue work items.  
  
```  
  
HANDLE GetQueueHandle( ) throw( );  
  
```  
  
### Return Value  
 Returns the queue handle or NULL if the thread pool has not been initialized.  
  
##  <a name="cthreadpool__getsize"></a>  CThreadPool::GetSize  
 Call this method to get the number of threads in the pool.  
  
```  
  
HRESULT STDMETHODCALLTYPE GetSize(  
      int*  pnNumThreads  
   ) throw( );  
  
```  
  
### Parameters  
 `pnNumThreads`  
 [out] Address of the variable that, on success, receives the number of threads in the pool.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="cthreadpool__gettimeout"></a>  CThreadPool::GetTimeout  
 Call this method to get the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
```  
  
HRESULT STDMETHODCALLTYPE GetTimeout(  
      DWORD*  pdwMaxWait  
   ) throw( );  
  
```  
  
### Parameters  
 `pdwMaxWait`  
 [out] Address of the variable that, on success, receives the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 This timeout value is used by [CThreadPool::Shutdown](../vs140/CThreadPool--Shutdown.md) if no other value is supplied to that method.  
  
##  <a name="cthreadpool__initialize"></a>  CThreadPool::Initialize  
 Call this method to initialize the thread pool.  
  
```  
  
HRESULT Initialize(  
      void *  pvWorkerParam  
    = NULL,  
      int  nNumThreads  
    = 0,  
      DWORD  dwStackSize  
    = 0,  
      HANDLE  hCompletion  
    = INVALID_HANDLE_VALUE   
   ) throw( );  
  
```  
  
### Parameters  
 `pvWorkerParam`  
 The worker parameter to be passed to the worker thread object's `Initialize`,                                 **Execute**, and `Terminate` methods.  
  
 `nNumThreads`  
 The requested number of threads in the pool.  
  
 If `nNumThreads` is negative, its absolute value will be multiplied by the number of processors in the machine to get the total number of threads.  
  
 If `nNumThreads` is zero, [ATLS_DEFAULT_THREADSPERPROC](../vs140/ATLS_DEFAULT_THREADSPERPROC.md) will be multiplied by the number of processors in the machine to get the total number of threads.  
  
 `dwStackSize`  
 The stack size for each thread in the pool.  
  
 *hCompletion*  
 The handle of an object to associate with the completion port.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="cthreadpool__queryinterface"></a>  CThreadPool::QueryInterface  
 Implementation of **IUnknown::QueryInterface**.  
  
```  
  
HRESULT STDMETHODCALLTYPE QueryInterface(  
      REFIID  riid,  
      void**  ppv  
   ) throw( );  
  
```  
  
### Remarks  
 Objects of this class can be successfully queried for the **IUnknown** and [IThreadPoolConfig](../vs140/IThreadPoolConfig-Interface.md) interfaces.  
  
##  <a name="cthreadpool__queuerequest"></a>  CThreadPool::QueueRequest  
 Call this method to queue a work item to be handled by a thread in the pool.  
  
```  
  
BOOL QueueRequest(  
      Worker::RequestType  request  
   ) throw( );  
  
```  
  
### Parameters  
 `request`  
 The request to be queued.  
  
### Return Value  
 Returns TRUE on success, FALSE on failure.  
  
### Remarks  
 This method adds a work item to the queue. The threads in the pool pick items off the queue in the order in which they are received.  
  
##  <a name="cthreadpool__release"></a>  CThreadPool::Release  
 Implementation of `IUnknown::Release`.  
  
```  
  
ULONG STDMETHODCALLTYPE Release( ) throw( );  
  
```  
  
### Return Value  
 Always returns 1.  
  
### Remarks  
 This class does not implement lifetime control using reference counting.  
  
##  <a name="cthreadpool__setsize"></a>  CThreadPool::SetSize  
 Call this method to set the number of threads in the pool.  
  
```  
  
HRESULT STDMETHODCALLTYPE SetSize(  
      int  nNumThreads  
   ) throw( );  
  
```  
  
### Parameters  
 `nNumThreads`  
 The requested number of threads in the pool.  
  
 If `nNumThreads` is negative, its absolute value will be multiplied by the number of processors in the machine to get the total number of threads.  
  
 If `nNumThreads` is zero, [ATLS_DEFAULT_THREADSPERPROC](../vs140/ATLS_DEFAULT_THREADSPERPROC.md) will be multiplied by the number of processors in the machine to get the total number of threads.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 If the number of threads specified is less than the number of threads currently in the pool, the object puts a shutdown message on the queue to be picked up by a waiting thread. When a waiting thread pulls the message off the queue, it notifies the thread pool and exits the thread procedure. This process is repeated until the number of threads in the pool reaches the specified number or until no thread has exited within the period specified by [GetTimeout](../vs140/CThreadPool--GetTimeout.md)/ [SetTimeout](../vs140/CThreadPool--SetTimeout.md). In this situation the method will return an HRESULT corresponding to **WAIT_TIMEOUT** and the pending shutdown message is canceled.  
  
##  <a name="cthreadpool__settimeout"></a>  CThreadPool::SetTimeout  
 Call this method to set the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
```  
  
HRESULT STDMETHODCALLTYPE SetTimeout(  
      DWORD  dwMaxWait  
   ) throw( );  
  
```  
  
### Parameters  
 `dwMaxWait`  
 The requested maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 The timeout is initialized to [ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT](../vs140/ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT.md) in the constructor.  
  
 Note that `dwMaxWait` is the time that the pool will wait for a single thread to shut down. The maximum time that could be taken to remove multiple threads from the pool could be slightly less than `dwMaxWait` multiplied by the number of threads.  
  
##  <a name="cthreadpool__shutdown"></a>  CThreadPool::Shutdown  
 Call this method to shut down the thread pool.  
  
```  
  
void Shutdown(  
      DWORD  dwMaxWait  
    = 0  
   ) throw( );  
  
```  
  
### Parameters  
 `dwMaxWait`  
 The requested maximum time in milliseconds that the thread pool will wait for a thread to shut down. If 0 or no value is supplied, this method will use the timeout set by [CThreadPool::SetTimeout](../vs140/CThreadPool--SetTimeout.md).  
  
### Remarks  
 This method posts a shutdown request to all threads in the pool. If the timeout expires, this method will call [TerminateThread](http://msdn.microsoft.com/library/windows/desktop/ms686717) on any thread that did not exit. This method is called automatically from the destructor of the class.  
  
## See Also  
 [IThreadPoolConfig Interface](../vs140/IThreadPoolConfig-Interface.md)   
 [DefaultThreadTraits](../vs140/DefaultThreadTraits.md)   
 [ATL Classes](../vs140/ATL-Classes.md)