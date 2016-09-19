---
title: "CMFCDropDownToolbarButton::OnClick"
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
ms.assetid: 8d440a91-9d2a-4989-9e17-5ccebfd1eaf1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::OnClick
Called by the framework when the user clicks the mouse button.  
  
## Syntax  
  
```  
virtual BOOL OnClick(  
   CWnd* pWnd,  
   BOOL bDelay = TRUE  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 The parent window of the toolbar button.  
  
 [in] `bDelay`  
 `TRUE` if the message should be handled with a delay.  
  
## Return Value  
 Nonzero if the button processes the click message; otherwise 0.  
  
## Remarks  
 This method extends the base class implementation, [CMFCToolBarButton::OnClick](../vs140/CMFCToolBarButton--OnClick.md), by updating the state of the drop-down toolbar.  
  
 When a user clicks the toolbar button, this method creates a timer that waits the length of time specified by the [CMFCDropDownToolbarButton::m_uiShowBarDelay](../vs140/CMFCDropDownToolbarButton--m_uiShowBarDelay.md) data member and then opens the drop-down toolbar by using the [CMFCDropDownToolbarButton::DropDownToolbar](../vs140/CMFCDropDownToolbarButton--DropDownToolbar.md) method. This method closes the drop-down toolbar the second time the user clicks the toolbar button.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnClick](../vs140/CMFCToolBarButton--OnClick.md)   
 [CMFCDropDownToolbarButton::m_uiShowBarDelay](../vs140/CMFCDropDownToolbarButton--m_uiShowBarDelay.md)   
 [CMFCDropDownToolbarButton::DropDownToolbar](../vs140/CMFCDropDownToolbarButton--DropDownToolbar.md)