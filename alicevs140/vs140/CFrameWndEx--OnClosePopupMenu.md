---
title: "CFrameWndEx::OnClosePopupMenu"
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
ms.assetid: 07ffc236-db46-4d6b-b5ff-a1dd6a173841
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnClosePopupMenu
Called by the framework when an active pop-up menu processes a WM_DESTROY message.  
  
## Syntax  
  
```  
virtual void OnClosePopupMenu(  
   CMFCPopupMenu* pMenuPopup   
);  
```  
  
#### Parameters  
 `pMenuPopup`  
 A pointer to a pop-up menu.  
  
## Remarks  
 The framework sends a WM_DESTROY message when it is about to close the window. Override this method if you want to handle notifications from `CMFCPopupMenu` objects that belong to the frame window when a `CMFCPopupMenu` object is processing a `WM_DESTROY` message sent by the framework when the window is being closed.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)