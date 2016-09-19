---
title: "CFrameWnd::CreateView"
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
ms.assetid: f490fc29-b689-4e24-b266-837192be83f9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::CreateView
Call `CreateView` to create a view within a frame.  
  
## Syntax  
  
```  
  
      CWnd* CreateView(  
   CCreateContext* pContext,  
   UINT nID = AFX_IDW_PANE_FIRST   
);  
```  
  
#### Parameters  
 `pContext`  
 Specifies the type of view and document.  
  
 `nID`  
 The ID number of a view.  
  
## Return Value  
 Pointer to a `CWnd` object if successful; otherwise **NULL**.  
  
## Remarks  
 Use this member function to create "views" that are not `CView`-derived within a frame. After calling `CreateView`, you must manually set the view to active and set it to be visible; these tasks are not automatically performed by `CreateView`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)