---
title: "CWinThread::SetThreadPriority"
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
ms.assetid: 64a5499f-545c-48c3-9003-470a41ee001f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::SetThreadPriority
This function sets the priority level of the current thread within its priority class.  
  
## Syntax  
  
```  
  
      BOOL SetThreadPriority(  
   int nPriority   
);  
```  
  
#### Parameters  
 `nPriority`  
 Specifies the new thread priority level within its priority class. This parameter must be one of the following values, listed from highest priority to lowest:  
  
-   **THREAD_PRIORITY_TIME_CRITICAL**  
  
-   **THREAD_PRIORITY_HIGHEST**  
  
-   **THREAD_PRIORITY_ABOVE_NORMAL**  
  
-   **THREAD_PRIORITY_NORMAL**  
  
-   **THREAD_PRIORITY_BELOW_NORMAL**  
  
-   **THREAD_PRIORITY_LOWEST**  
  
-   **THREAD_PRIORITY_IDLE**  
  
 For more information on these priorities, see [SetThreadPriority](http://msdn.microsoft.com/library/windows/desktop/ms686277) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if function was successful; otherwise 0.  
  
## Remarks  
 It can only be called after [CreateThread](../vs140/CWinThread--CreateThread.md) successfully returns.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinThread::GetThreadPriority](../vs140/CWinThread--GetThreadPriority.md)   
 [SetThreadPriority](http://msdn.microsoft.com/library/windows/desktop/ms686277)