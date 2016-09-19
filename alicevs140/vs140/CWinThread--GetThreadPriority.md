---
title: "CWinThread::GetThreadPriority"
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
ms.assetid: d85c7f70-0c8d-450e-8a4d-300195c54cf7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::GetThreadPriority
Gets the current thread priority level of this thread.  
  
## Syntax  
  
```  
  
int GetThreadPriority( );  
```  
  
## Return Value  
 The current thread priority level within its priority class. The value returned will be one of the following, listed from highest priority to lowest:  
  
-   **THREAD_PRIORITY_TIME_CRITICAL**  
  
-   **THREAD_PRIORITY_HIGHEST**  
  
-   **THREAD_PRIORITY_ABOVE_NORMAL**  
  
-   **THREAD_PRIORITY_NORMAL**  
  
-   **THREAD_PRIORITY_BELOW_NORMAL**  
  
-   **THREAD_PRIORITY_LOWEST**  
  
-   **THREAD_PRIORITY_IDLE**  
  
 For more information on these priorities, see [SetThreadPriority](http://msdn.microsoft.com/library/windows/desktop/ms686277) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinThread::SetThreadPriority](../vs140/CWinThread--SetThreadPriority.md)   
 [GetThreadPriority](http://msdn.microsoft.com/library/windows/desktop/ms683235)