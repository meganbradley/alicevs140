---
title: "CMFCToolBar::InvalidateButton"
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
ms.assetid: 7ee50764-820d-42ee-a460-5f10ed7b53a2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::InvalidateButton
Invalidates the client area of the toolbar button that exists at the provided index.  
  
## Syntax  
  
```  
CMFCToolBarButton* InvalidateButton(  
   int nIndex  
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index of the button in the toolbar.  
  
## Return Value  
 A pointer to the `CMFCToolBarButton` object that exists at the provided index or `NULL` if no such object exists.  
  
## Remarks  
 The framework calls this method when it updates the client area that is associated with a toolbar button. It calls the [CWnd::InvalidateRect](../vs140/CWnd--InvalidateRect.md) method with the client rectangle of the `CMFCToolBarButton` object that exists at the provided index.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWnd::InvalidateRect](../vs140/CWnd--InvalidateRect.md)