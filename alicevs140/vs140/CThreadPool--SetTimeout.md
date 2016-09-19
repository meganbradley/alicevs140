---
title: "CThreadPool::SetTimeout"
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
ms.assetid: 9efa62b1-9512-4e12-bddc-274483088f07
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CThreadPool::SetTimeout
Call this method to set the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE SetTimeout(  
   DWORD dwMaxWait   
) throw( );  
```  
  
#### Parameters  
 `dwMaxWait`  
 The requested maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The timeout is initialized to [ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT](../vs140/ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT.md) in the constructor.  
  
 Note that `dwMaxWait` is the time that the pool will wait for a single thread to shut down. The maximum time that could be taken to remove multiple threads from the pool could be slightly less than `dwMaxWait` multiplied by the number of threads.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CThreadPool Class](../vs140/CThreadPool-Class.md)   
 [IThreadPoolConfig::SetTimeout](../vs140/IThreadPoolConfig--SetTimeout.md)   
 [CThreadPool::GetTimeout](../vs140/CThreadPool--GetTimeout.md)