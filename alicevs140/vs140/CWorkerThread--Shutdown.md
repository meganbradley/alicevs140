---
title: "CWorkerThread::Shutdown"
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
ms.assetid: 79494ba2-052c-483e-8fb1-593087444bfd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWorkerThread::Shutdown
Call this method to shut down the worker thread.  
  
## Syntax  
  
```  
  
      HRESULT Shutdown(  
   DWORD dwWait = ATL_WORKER_THREAD_WAIT   
) throw( );  
```  
  
#### Parameters  
 `dwWait`  
 The time in milliseconds to wait for the worker thread to shut down.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure, such as if the timeout value, `dwWait`, is exceeded.  
  
## Remarks  
 To reuse the object, call [CWorkerThread::Initialize](../vs140/CWorkerThread--Initialize.md) after calling this method.  
  
 Note that calling **Shutdown** on an object initialized with a pointer to another `CWorkerThread` object has no effect and always returns S_OK.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CWorkerThread Class](../vs140/CWorkerThread-Class.md)   
 [ATL_WORKER_THREAD_WAIT](../vs140/ATL_WORKER_THREAD_WAIT.md)