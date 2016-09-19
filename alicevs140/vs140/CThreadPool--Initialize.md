---
title: "CThreadPool::Initialize"
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
ms.assetid: 78eeeb4f-8ecb-46a9-8d65-832ebe2e9379
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CThreadPool::Initialize
Call this method to initialize the thread pool.  
  
## Syntax  
  
```  
  
      HRESULT Initialize(  
   void * pvWorkerParam = NULL,  
   int nNumThreads = 0,  
   DWORD dwStackSize = 0,  
   HANDLE hCompletion = INVALID_HANDLE_VALUE   
) throw( );  
```  
  
#### Parameters  
 `pvWorkerParam`  
 The worker parameter to be passed to the worker thread object's `Initialize`, **Execute**, and `Terminate` methods.  
  
 `nNumThreads`  
 The requested number of threads in the pool.  
  
 If `nNumThreads` is negative, its absolute value will be multiplied by the number of processors in the machine to get the total number of threads.  
  
 If `nNumThreads` is zero, [ATLS_DEFAULT_THREADSPERPROC](../vs140/ATLS_DEFAULT_THREADSPERPROC.md) will be multiplied by the number of processors in the machine to get the total number of threads.  
  
 `dwStackSize`  
 The stack size for each thread in the pool.  
  
 *hCompletion*  
 The handle of an object to associate with the completion port.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CThreadPool Class](../vs140/CThreadPool-Class.md)