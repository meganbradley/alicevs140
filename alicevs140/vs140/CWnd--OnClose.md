---
title: "CWnd::OnClose"
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
ms.assetid: aeafcdae-f35e-4bb4-8cd3-3af1226decf7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnClose
The framework calls this member function as a signal that the `CWnd` or an application is to terminate.  
  
## Syntax  
  
```  
  
afx_msg void OnClose( );  
```  
  
## Remarks  
 The default implementation calls `DestroyWindow`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md)   
 [WM_CLOSE](http://msdn.microsoft.com/library/windows/desktop/ms632617)