---
title: "CWorkerThread::GetThreadHandle"
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
ms.assetid: 987e458c-35c7-4990-9dd5-9fc4a7b8e84b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWorkerThread::GetThreadHandle
Call this method to get the thread handle of the worker thread.  
  
## Syntax  
  
```  
  
HANDLE GetThreadHandle( ) throw( );  
  
```  
  
## Return Value  
 Returns the thread handle or NULL if the worker thread has not been initialized.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CWorkerThread Class](../vs140/CWorkerThread-Class.md)