---
title: "CWinApp::ProcessWndProcException"
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
ms.assetid: 15ed56fe-deee-4a69-b0df-68a457ab4840
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::ProcessWndProcException
The framework calls this member function whenever the handler does not catch an exception thrown in one of your application's message or command handlers.  
  
## Syntax  
  
```  
  
      virtual LRESULT ProcessWndProcException(  
   CException* e,  
   const MSG* pMsg   
);  
```  
  
#### Parameters  
 *e*  
 A pointer to an uncaught exception.  
  
 `pMsg`  
 A [MSG](../vs140/MSG-Structure.md) structure that contains information about the windows message that caused the framework to throw an exception.  
  
## Return Value  
 The value that should be returned to Windows. Normally this is 0L for windows messages, 1L (**TRUE**) for command messages.  
  
## Remarks  
 Do not call this member function directly.  
  
 The default implementation of this member function creates a message box. If the uncaught exception originates with a menu, toolbar, or accelerator command failure, the message box displays a "Command failed" message; otherwise, it displays an "Internal application error" message.  
  
 Override this member function to provide global handling of your exceptions. Only call the base functionality if you wish the message box to be displayed.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::WindowProc](../vs140/CWnd--WindowProc.md)   
 [CException Class](../vs140/CException-Class.md)