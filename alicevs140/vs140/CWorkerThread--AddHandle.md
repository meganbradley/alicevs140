---
title: "CWorkerThread::AddHandle"
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
ms.assetid: 30baeb7c-aa16-43c0-a947-ff65f6a7f145
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWorkerThread::AddHandle
Call this method to add a waitable object's handle to the list maintained by the worker thread.  
  
## Syntax  
  
```  
  
      HRESULT AddHandle(  
   HANDLE hObject,  
   IWorkerThreadClient* pClient,  
   DWORD_PTR dwParam   
) throw( );  
```  
  
#### Parameters  
 `hObject`  
 The handle to a waitable object.  
  
 `pClient`  
 The pointer to the [IWorkerThreadClient](../vs140/IWorkerThreadClient-Interface.md) interface on the object to be called when the handle is signaled.  
  
 `dwParam`  
 The parameter to be passed to [IWorkerThreadClient::Execute](../vs140/IWorkerThreadClient--Execute.md) when the handle is signaled.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 [IWorkerThreadClient::Execute](../vs140/IWorkerThreadClient--Execute.md) will be called through `pClient` when the handle, `hObject`, is signaled.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CWorkerThread Class](../vs140/CWorkerThread-Class.md)