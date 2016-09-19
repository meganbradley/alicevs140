---
title: "CView::OnActivateFrame"
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
ms.assetid: fb844e96-8dec-41ac-bc95-314d95455c72
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnActivateFrame
Called by the framework when the frame window containing the view is activated or deactivated.  
  
## Syntax  
  
```  
  
      virtual void OnActivateFrame(  
   UINT nState,  
   CFrameWnd* pFrameWnd   
);  
```  
  
#### Parameters  
 `nState`  
 Specifies whether the frame window is being activated or deactivated. It can be one of the following values:  
  
-   **WA_INACTIVE** The frame window is being deactivated.  
  
-   **WA_ACTIVE** The frame window is being activated through some method other than a mouse click (for example, by use of the keyboard interface to select the window).  
  
-   **WA_CLICKACTIVE** The frame window is being activated by a mouse click  
  
 `pFrameWnd`  
 Pointer to the frame window that is to be activated.  
  
## Remarks  
 Override this member function if you want to perform special processing when the frame window associated with the view is activated or deactivated. For example, [CFormView](../vs140/CFormView-Class.md) performs this override when it saves and restores the control that has focus.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnActivate](../vs140/CWnd--OnActivate.md)   
 [CFormView Class](../vs140/CFormView-Class.md)