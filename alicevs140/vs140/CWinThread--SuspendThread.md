---
title: "CWinThread::SuspendThread"
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
ms.assetid: 57189c7e-fd71-42e5-bc4b-3de7cd373d28
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::SuspendThread
Increments the current thread's suspend count.  
  
## Syntax  
  
```  
  
DWORD SuspendThread( );  
```  
  
## Return Value  
 The thread's previous suspend count if successful; `0xFFFFFFFF` otherwise.  
  
## Remarks  
 If any thread has a suspend count above zero, that thread does not execute. The thread can be resumed by calling the [ResumeThread](../vs140/CWinThread--ResumeThread.md) member function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinThread::ResumeThread](../vs140/CWinThread--ResumeThread.md)   
 [SuspendThread](http://msdn.microsoft.com/library/windows/desktop/ms686345)