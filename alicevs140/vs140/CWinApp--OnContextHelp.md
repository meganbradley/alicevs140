---
title: "CWinApp::OnContextHelp"
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
ms.assetid: 713d9a27-e3e3-45b1-a151-e0ed30b29b32
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::OnContextHelp
Handles SHIFT+F1 Help within the application.  
  
## Syntax  
  
```  
  
afx_msg void OnContextHelp( );  
```  
  
## Remarks  
 You must add an `ON_COMMAND( ID_CONTEXT_HELP, OnContextHelp )` statement to your `CWinApp` class message map and also add an accelerator table entry, typically SHIFT+F1, to enable this member function.  
  
 `OnContextHelp` puts the application into Help mode. The cursor changes to an arrow and a question mark, and the user can then move the mouse pointer and press the left mouse button to select a dialog box, window, menu, or command button. This member function retrieves the Help context of the object under the cursor and calls the Windows function WinHelp with that Help context.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnHelp](../vs140/CWinApp--OnHelp.md)   
 [CWinApp::WinHelp](../vs140/CWinApp--WinHelp.md)