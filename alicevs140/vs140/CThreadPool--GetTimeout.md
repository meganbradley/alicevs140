---
title: "CThreadPool::GetTimeout"
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
ms.assetid: f27db84b-a4fd-42e1-9c83-89f0458e43e8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CThreadPool::GetTimeout
Call this method to get the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE GetTimeout(  
   DWORD* pdwMaxWait   
) throw( );  
```  
  
#### Parameters  
 `pdwMaxWait`  
 [out] Address of the variable that, on success, receives the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This timeout value is used by [CThreadPool::Shutdown](../vs140/CThreadPool--Shutdown.md) if no other value is supplied to that method.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CThreadPool Class](../vs140/CThreadPool-Class.md)   
 [IThreadPoolConfig::GetTimeout](../vs140/IThreadPoolConfig--GetTimeout.md)   
 [CThreadPool::SetTimeout](../vs140/CThreadPool--SetTimeout.md)