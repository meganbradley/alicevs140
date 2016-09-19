---
title: "CWnd::ChangeClipboardChain"
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
ms.assetid: 350c9f51-ddef-4ae6-9886-db5d96bebf86
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ChangeClipboardChain
Removes `CWnd` from the chain of Clipboard viewers and makes the window specified by `hWndNext` the descendant of the `CWnd` ancestor in the chain.  
  
## Syntax  
  
```  
  
      BOOL ChangeClipboardChain(  
   HWND hWndNext   
);  
```  
  
#### Parameters  
 `hWndNext`  
 Identifies the window that follows `CWnd` in the Clipboard-viewer chain.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetClipboardViewer](../vs140/CWnd--SetClipboardViewer.md)   
 [ChangeClipboardChain](http://msdn.microsoft.com/library/windows/desktop/ms649034)