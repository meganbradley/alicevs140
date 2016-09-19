---
title: "CThreadPool::Shutdown"
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
ms.assetid: c955f747-e6e6-4865-a9bb-11a89f4de57b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CThreadPool::Shutdown
Call this method to shut down the thread pool.  
  
## Syntax  
  
```  
  
      void Shutdown(  
   DWORD dwMaxWait = 0  
) throw( );  
```  
  
#### Parameters  
 `dwMaxWait`  
 The requested maximum time in milliseconds that the thread pool will wait for a thread to shut down. If 0 or no value is supplied, this method will use the timeout set by [CThreadPool::SetTimeout](../vs140/CThreadPool--SetTimeout.md).  
  
## Remarks  
 This method posts a shutdown request to all threads in the pool. If the timeout expires, this method will call [TerminateThread](http://msdn.microsoft.com/library/windows/desktop/ms686717) on any thread that did not exit. This method is called automatically from the destructor of the class.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CThreadPool Class](../vs140/CThreadPool-Class.md)