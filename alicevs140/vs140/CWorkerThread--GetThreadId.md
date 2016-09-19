---
title: "CWorkerThread::GetThreadId"
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
ms.assetid: 27abeb97-b089-4ddc-a044-661e04fa4cdd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWorkerThread::GetThreadId
Call this method to get the thread ID of the worker thread.  
  
## Syntax  
  
```  
  
DWORD GetThreadId( ) throw( );  
  
```  
  
## Return Value  
 Returns the thread ID or NULL if the worker thread has not been initialized.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CWorkerThread Class](../vs140/CWorkerThread-Class.md)