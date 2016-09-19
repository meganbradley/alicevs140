---
title: "CWnd::OnQueryNewPalette"
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
ms.assetid: 3bbf0a2d-9004-4298-b781-e1bb74f7eb0a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnQueryNewPalette
The framework calls this member function when the `CWnd` object is about to receive the input focus, giving the `CWnd` an opportunity to realize its logical palette when it receives the focus.  
  
## Syntax  
  
```  
  
afx_msg BOOL OnQueryNewPalette( );  
```  
  
## Return Value  
 Nonzero if the `CWnd` realizes its logical palette; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Default](../vs140/CWnd--Default.md)   
 [CWnd::OnPaletteChanged](../vs140/CWnd--OnPaletteChanged.md)   
 [WM_QUERYNEWPALETTE](http://msdn.microsoft.com/library/windows/desktop/dd145218)