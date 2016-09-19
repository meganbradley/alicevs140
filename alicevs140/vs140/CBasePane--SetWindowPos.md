---
title: "CBasePane::SetWindowPos"
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
ms.assetid: 28c23155-6660-4d70-8912-4c59d52a3390
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::SetWindowPos
Changes the size, position, and Z-order of a pane.  
  
## Syntax  
  
```  
virtual HDWP SetWindowPos(  
   const CWnd* pWndInsertAfter,  
   int x,  
   int y,  
   int cx,  
   int cy,  
   UINT nFlags,  
   HDWP hdwp = NULL  
);  
```  
  
#### Parameters  
 [in] `pWndInsertAfter`  
 Identifies the `CWnd` object that comes before this `CWnd` object in the Z-order. For more information, see [CWnd::SetWindowPos](../vs140/CWnd--SetWindowPos.md).  
  
 [in] `x`  
 Specifies the position of the left side of the window.  
  
 [in] `y`  
 Specifies the position of the top of the window.  
  
 [in] `cx`  
 Specifies the width of the window.  
  
 [in] `cy`  
 Specifies the height of the window.  
  
 [in] `nFlags`  
 Specifies size and position options. For more information, see [CWnd::SetWindowPos](../vs140/CWnd--SetWindowPos.md).  
  
 [in] `hdwp`  
 Handle to a structure that contains size and position information for one or more windows.  
  
## Return Value  
 A handle to an updated deferred window position structure, or `NULL`.  
  
## Remarks  
 If `pWndInsertAfter` is `NULL`, this method calls [CWnd::SetWindowPos](../vs140/CWnd--SetWindowPos.md). If `pWndInsertAfter` is non-`NULL`, this method calls `DeferWindowPos`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)