---
title: "CWinApp::Run"
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
ms.assetid: aea0d215-f6be-4f40-bfae-939db926775f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::Run
Provides a default message loop.  
  
## Syntax  
  
```  
  
virtual int Run( );  
```  
  
## Return Value  
 An `int` value that is returned by `WinMain`.  
  
## Remarks  
 **Run** acquires and dispatches Windows messages until the application receives a **WM_QUIT** message. If the application's message queue currently contains no messages, **Run** calls [OnIdle](../vs140/CWinApp--OnIdle.md) to perform idle-time processing. Incoming messages go to the [PreTranslateMessage](../vs140/CWinApp--PreTranslateMessage.md) member function for special processing and then to the Windows function **TranslateMessage** for standard keyboard translation; finally, the **DispatchMessage** Windows function is called.  
  
 **Run** is rarely overridden, but you can override it to provide special behavior.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::PreTranslateMessage](../vs140/CWinApp--PreTranslateMessage.md)   
 [WM_QUIT](http://msdn.microsoft.com/library/windows/desktop/ms632641)   
 [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934)   
 [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955)