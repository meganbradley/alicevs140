---
title: "CNoWorkerThread::Shutdown"
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
ms.assetid: 74dd13b9-e8db-470c-add7-387af5ee632f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNoWorkerThread::Shutdown
Non-functional equivalent of [CWorkerThread::Shutdown](../vs140/CWorkerThread--Shutdown.md).  
  
## Syntax  
  
```  
  
      HRESULT Shutdown(  
   DWORD dwWait = ATL_WORKER_THREAD_WAIT   
) throw( );  
```  
  
## Return Value  
 Always returns S_OK.  
  
## Remarks  
 The implementation provided by this class does nothing.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CNoWorkerThread Class](../vs140/CNoWorkerThread-Class.md)