---
title: "CWorkerThread::AddTimer"
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
ms.assetid: cc3770f1-25bc-4767-afb9-d9ccdb17e29e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWorkerThread::AddTimer
Call this method to add a periodic waitable timer to the list maintained by the worker thread.  
  
## Syntax  
  
```  
  
      HRESULT AddTimer(  
   DWORD dwInterval,  
   IWorkerThreadClient* pClient,  
   DWORD_PTR dwParam,  
   HANDLE* phTimer  
) throw( );  
```  
  
#### Parameters  
 *dwInterval*  
 Specifies the period of the timer in milliseconds.  
  
 `pClient`  
 The pointer to the [IWorkerThreadClient](../vs140/IWorkerThreadClient-Interface.md) interface on the object to be called when the handle is signaled.  
  
 `dwParam`  
 The parameter to be passed to [IWorkerThreadClient::Execute](../vs140/IWorkerThreadClient--Execute.md) when the handle is signaled.  
  
 `phTimer`  
 [out] Address of the HANDLE variable that, on success, receives the handle to the newly created timer.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 [IWorkerThreadClient::Execute](../vs140/IWorkerThreadClient--Execute.md) will be called through `pClient` when the timer is signaled.  
  
 Pass the timer handle from `phTimer` to [CWorkerThread::RemoveHandle](../vs140/CWorkerThread--RemoveHandle.md) to close the timer.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CWorkerThread Class](../vs140/CWorkerThread-Class.md)