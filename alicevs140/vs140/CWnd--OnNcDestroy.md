---
title: "CWnd::OnNcDestroy"
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
ms.assetid: 00c8609a-d93d-4c26-ba7b-32bb27f50c15
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnNcDestroy
Called by the framework when the nonclient area is being destroyed, and is the last member function called when the Windows window is destroyed.  
  
## Syntax  
  
```  
  
afx_msg void OnNcDestroy( );  
```  
  
## Remarks  
 The default implementation performs some cleanup, then calls the virtual member function [PostNcDestroy](../vs140/CWnd--PostNcDestroy.md).  
  
 Override `PostNcDestroy` if you want to perform your own cleanup, such as a **delete this** operation. If you override `OnNcDestroy`, you must call `OnNcDestroy` in your base class to ensure that any memory internally allocated for the window is freed.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md)   
 [CWnd::OnNcCreate](../vs140/CWnd--OnNcCreate.md)   
 [WM_NCDESTROY](http://msdn.microsoft.com/library/windows/desktop/ms632636)   
 [CWnd::Default](../vs140/CWnd--Default.md)   
 [CWnd::PostNcDestroy](../vs140/CWnd--PostNcDestroy.md)