---
title: "CWnd::UnsubclassWindow"
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
ms.assetid: efe988a1-40f0-4c1e-9145-b2e0fdf279fa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::UnsubclassWindow
Call this member function to set **WndProc** back to its original value and detach the window identified by `HWND` from the **CWnd** object.  
  
## Syntax  
  
```  
  
HWND UnsubclassWindow( );  
```  
  
## Return Value  
 A handle to the unsubclassed window.  
  
## Example  
 See the example for [CWnd::SubclassWindow](../vs140/CWnd--SubclassWindow.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SubclassWindow](../vs140/CWnd--SubclassWindow.md)   
 [CWnd::PreSubclassWindow](../vs140/CWnd--PreSubclassWindow.md)   
 [CWnd::DefWindowProc](../vs140/CWnd--DefWindowProc.md)   
 [CWnd::SubclassDlgItem](../vs140/CWnd--SubclassDlgItem.md)   
 [CWnd::Attach](../vs140/CWnd--Attach.md)