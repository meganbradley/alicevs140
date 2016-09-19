---
title: "CWinThread::ResumeThread"
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
ms.assetid: d6f97a2f-5c9f-4ee1-b978-d74938784db5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::ResumeThread
Called to resume execution of a thread that was suspended by the [SuspendThread](../vs140/CWinThread--SuspendThread.md) member function, or a thread created with the **CREATE_SUSPENDED** flag.  
  
## Syntax  
  
```  
  
DWORD ResumeThread( );  
```  
  
## Return Value  
 The thread's previous suspend count if successful; `0xFFFFFFFF` otherwise. If the return value is zero, the current thread was not suspended. If the return value is one, the thread was suspended, but is now restarted. Any return value greater than one means the thread remains suspended.  
  
## Remarks  
 The suspend count of the current thread is reduced by one. If the suspend count is reduced to zero, the thread resumes execution; otherwise the thread remains suspended.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ResumeThread](http://msdn.microsoft.com/library/windows/desktop/ms685086)   
 [CWinThread::m_bAutoDelete](../vs140/CWinThread--m_bAutoDelete.md)   
 [AfxBeginThread](../vs140/AfxBeginThread.md)