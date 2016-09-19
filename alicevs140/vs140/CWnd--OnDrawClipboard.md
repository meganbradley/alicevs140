---
title: "CWnd::OnDrawClipboard"
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
ms.assetid: 37c84660-2d52-4f73-808b-df34642ee820
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnDrawClipboard
The framework calls this member function for each window in the Clipboard-viewer chain when the contents of the Clipboard change.  
  
## Syntax  
  
```  
  
afx_msg void OnDrawClipboard( );  
```  
  
## Remarks  
 Only applications that have joined the Clipboard-viewer chain by calling the [SetClipboardViewer](../vs140/CWnd--SetClipboardViewer.md) member function need to respond to this call.  
  
 Each window that receives an `OnDrawClipboard` call should call the [SendMessage](http://msdn.microsoft.com/library/windows/desktop/ms644950) Windows function to pass a [WM_DRAWCLIPBOARD](http://msdn.microsoft.com/library/windows/desktop/ms649025) message on to the next window in the Clipboard-viewer chain. The handle of the next window is returned by the [SetClipboardViewer](../vs140/CWnd--SetClipboardViewer.md) member function; it may be modified in response to an [OnChangeCbChain](../vs140/CWnd--OnChangeCbChain.md) member function call.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SendMessage](http://msdn.microsoft.com/library/windows/desktop/ms644950)   
 [CWnd::SetClipboardViewer](../vs140/CWnd--SetClipboardViewer.md)   
 [CWnd::OnChangeCbChain](../vs140/CWnd--OnChangeCbChain.md)   
 [WM_DRAWCLIPBOARD](http://msdn.microsoft.com/library/windows/desktop/ms649025)