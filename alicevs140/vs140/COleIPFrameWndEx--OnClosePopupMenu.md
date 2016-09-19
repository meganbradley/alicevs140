---
title: "COleIPFrameWndEx::OnClosePopupMenu"
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
ms.assetid: 67646508-24b3-41e2-9518-4900de67ab0e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::OnClosePopupMenu
Called by the framework when an active pop-up menu processes a `WM_DESTROY` message.  
  
## Syntax  
  
```  
virtual void OnClosePopupMenu(  
   CMFCPopupMenu* pMenuPopup   
);  
```  
  
#### Parameters  
 [in] `pMenuPopup`  
 A pointer to the pop-up menu object.  
  
## Remarks  
 Override this method to receive notifications from `CMFCPopupMenu` objects when they process `WM_DESTROY` messages.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)