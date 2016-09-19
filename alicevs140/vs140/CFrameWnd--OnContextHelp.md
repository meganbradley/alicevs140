---
title: "CFrameWnd::OnContextHelp"
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
ms.assetid: 4be7bbf3-17ac-4bdb-a187-c598cbfece94
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::OnContextHelp
Handles SHIFT+F1 Help for in-place items.  
  
## Syntax  
  
```  
  
afx_msg void OnContextHelp( );  
```  
  
## Remarks  
 To enable context-sensitive help, you must add an  
  
 [!CODE [NVC_MFCDocViewSDI#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocViewSDI#16)]  
  
 statement to your `CFrameWnd` class message map and also add an accelerator-table entry, typically SHIFT+F1, to enable this member function.  
  
 If your application is an OLE Container, `OnContextHelp` puts all in-place items contained within the frame window object into Help mode. The cursor changes to an arrow and a question mark, and the user can then move the mouse pointer and press the left mouse button to select a dialog box, window, menu, or command button. This member function calls the Windows function `WinHelp` with the Help context of the object under the cursor.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnHelp](../vs140/CWinApp--OnHelp.md)   
 [CWinApp::WinHelp](../vs140/CWinApp--WinHelp.md)