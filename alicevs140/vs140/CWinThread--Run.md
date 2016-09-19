---
title: "CWinThread::Run"
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
ms.assetid: 1aa41001-7295-4159-a8f9-74d460acd1b1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::Run
Provides a default message loop for user-interface threads.  
  
## Syntax  
  
```  
  
virtual int Run( );  
```  
  
## Return Value  
 An `int` value that is returned by the thread. This value can be retrieved by calling [GetExitCodeThread](http://msdn.microsoft.com/library/windows/desktop/ms683190).  
  
## Remarks  
 **Run** acquires and dispatches Windows messages until the application receives a [WM_QUIT](http://msdn.microsoft.com/library/windows/desktop/ms632641) message. If the thread's message queue currently contains no messages, **Run** calls `OnIdle` to perform idle-time processing. Incoming messages go to the [PreTranslateMessage](../vs140/CWinThread--PreTranslateMessage.md) member function for special processing and then to the Windows function [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955) for standard keyboard translation. Finally, the [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934) Windows function is called.  
  
 **Run** is rarely overridden, but you can override it to implement special behavior.  
  
 This member function is used only in user-interface threads.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::Run](../vs140/CWinApp--Run.md)