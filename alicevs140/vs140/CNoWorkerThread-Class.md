---
title: "CNoWorkerThread Class"
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
ms.assetid: 29f06bae-b658-4aac-9c14-331e996d25d1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNoWorkerThread Class
Use this class as the argument for the `MonitorClass` template parameter to cache classes if you want to disable dynamic cache maintenance.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CNoWorkerThread  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CNoWorkerThread::AddHandle](../vs140/CNoWorkerThread--AddHandle.md)|Non-functional equivalent of [CWorkerThread::AddHandle](../vs140/CWorkerThread--AddHandle.md).|  
|[CNoWorkerThread::AddTimer](../vs140/CNoWorkerThread--AddTimer.md)|Non-functional equivalent of [CWorkerThread::AddTimer](../vs140/CWorkerThread--AddTimer.md).|  
|[CNoWorkerThread::GetThreadHandle](../vs140/CNoWorkerThread--GetThreadHandle.md)|Non-functional equivalent of [CWorkerThread::GetThreadHandle](../vs140/CWorkerThread--GetThreadHandle.md).|  
|[CNoWorkerThread::GetThreadId](../vs140/CNoWorkerThread--GetThreadId.md)|Non-functional equivalent of [CWorkerThread::GetThreadId](../vs140/CWorkerThread--GetThreadId.md).|  
|[CNoWorkerThread::Initialize](../vs140/CNoWorkerThread--Initialize.md)|Non-functional equivalent of [CWorkerThread::Initialize](../vs140/CWorkerThread--Initialize.md).|  
|[CNoWorkerThread::RemoveHandle](../vs140/CNoWorkerThread--RemoveHandle.md)|Non-functional equivalent of [CWorkerThread::RemoveHandle](../vs140/CWorkerThread--RemoveHandle.md).|  
|[CNoWorkerThread::Shutdown](../vs140/CNoWorkerThread--Shutdown.md)|Non-functional equivalent of [CWorkerThread::Shutdown](../vs140/CWorkerThread--Shutdown.md).|  
  
## Remarks  
 This class provides the same public interface as [CWorkerThread](../vs140/CWorkerThread-Class.md). This interface is expected to be provided by the `MonitorClass` template parameter to cache classes.  
  
 The methods in this class are implemented to do nothing. The methods that return an HRESULT always return S_OK, and the methods that return a HANDLE or thread ID always return 0.  
  
## Requirements  
 **Header:** atlutil.h  
  
##  <a name="cnoworkerthread__addhandle"></a>  CNoWorkerThread::AddHandle  
 Non-functional equivalent of [CWorkerThread::AddHandle](../vs140/CWorkerThread--AddHandle.md).  
  
```  
  
HRESULT AddHandle(  
      HANDLE /*  hObject  
    */,  
      IWorkerThreadClient * /*  pClient  
    */,  
      DWORD_PTR /*  dwParam  
    */   
   ) throw( );  
  
```  
  
### Return Value  
 Always returns S_OK.  
  
### Remarks  
 The implementation provided by this class does nothing.  
  
##  <a name="cnoworkerthread__addtimer"></a>  CNoWorkerThread::AddTimer  
 Non-functional equivalent of [CWorkerThread::AddTimer](../vs140/CWorkerThread--AddTimer.md).  
  
```  
  
HRESULT AddTimer(  
      DWORD /*  dwInterval  
    */,  
      IWorkerThreadClient * /*  pClient  
    */,  
      DWORD_PTR /*  dwParam  
    */,  
      HANDLE * /*  phTimer  
    */   
   ) throw( );  
  
```  
  
### Return Value  
 Always returns S_OK.  
  
### Remarks  
 The implementation provided by this class does nothing.  
  
##  <a name="cnoworkerthread__getthreadhandle"></a>  CNoWorkerThread::GetThreadHandle  
 Non-functional equivalent of [CWorkerThread::GetThreadHandle](../vs140/CWorkerThread--GetThreadHandle.md).  
  
```  
  
HANDLE GetThreadHandle( ) throw( );  
  
```  
  
### Return Value  
 Always returns NULL.  
  
### Remarks  
 The implementation provided by this class does nothing.  
  
##  <a name="cnoworkerthread__getthreadid"></a>  CNoWorkerThread::GetThreadId  
 Non-functional equivalent of [CWorkerThread::GetThreadId](../vs140/CWorkerThread--GetThreadId.md).  
  
```  
  
DWORD GetThreadId( ) throw( );  
  
```  
  
### Return Value  
 Always returns 0.  
  
### Remarks  
 The implementation provided by this class does nothing.  
  
##  <a name="cnoworkerthread__initialize"></a>  CNoWorkerThread::Initialize  
 Non-functional equivalent of [CWorkerThread::Initialize](../vs140/CWorkerThread--Initialize.md).  
  
```  
  
HRESULT Initialize( ) throw( );  
  
```  
  
### Return Value  
 Always returns S_OK.  
  
### Remarks  
 The implementation provided by this class does nothing.  
  
##  <a name="cnoworkerthread__removehandle"></a>  CNoWorkerThread::RemoveHandle  
 Non-functional equivalent of [CWorkerThread::RemoveHandle](../vs140/CWorkerThread--RemoveHandle.md).  
  
```  
  
HRESULT RemoveHandle(  
      HANDLE /*  hObject  
    */   
   ) throw( );  
  
```  
  
### Return Value  
 Always returns S_OK.  
  
### Remarks  
 The implementation provided by this class does nothing.  
  
##  <a name="cnoworkerthread__shutdown"></a>  CNoWorkerThread::Shutdown  
 Non-functional equivalent of [CWorkerThread::Shutdown](../vs140/CWorkerThread--Shutdown.md).  
  
```  
  
HRESULT Shutdown(  
      DWORD  dwWait  
    = ATL_WORKER_THREAD_WAIT   
   ) throw( );  
  
```  
  
### Return Value  
 Always returns S_OK.  
  
### Remarks  
 The implementation provided by this class does nothing.