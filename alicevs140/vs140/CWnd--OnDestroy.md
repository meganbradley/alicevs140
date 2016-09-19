---
title: "CWnd::OnDestroy"
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
ms.assetid: 1cfc8ce5-1aba-4da6-bb5b-fe81d52dcda4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnDestroy
The framework calls this member function to inform the `CWnd` object that it is being destroyed.  
  
## Syntax  
  
```  
  
afx_msg void OnDestroy( );  
```  
  
## Remarks  
 `OnDestroy` is called after the `CWnd` object is removed from the screen.  
  
 `OnDestroy` is called first for the `CWnd` being destroyed, then for the child windows of `CWnd` as they are destroyed. It can be assumed that all child windows still exist while `OnDestroy` runs.  
  
 If the `CWnd` object being destroyed is part of the Clipboard-viewer chain (set by calling the [SetClipboardViewer](../vs140/CWnd--SetClipboardViewer.md) member function), the `CWnd` must remove itself from the Clipboard-viewer chain by calling the [ChangeClipboardChain](../vs140/CWnd--ChangeClipboardChain.md) member function before returning from the `OnDestroy` function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::ChangeClipboardChain](../vs140/CWnd--ChangeClipboardChain.md)   
 [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md)   
 [CWnd::SetClipboardViewer](../vs140/CWnd--SetClipboardViewer.md)