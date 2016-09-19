---
title: "CFrameWndEx::OnTearOffMenu"
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
ms.assetid: ca694fca-b819-4d6e-ba92-f60c1d5eee1c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnTearOffMenu
Called by the framework when the application displays a menu that has a tear-off bar.  
  
## Syntax  
  
```  
virtual BOOL OnTearOffMenu(  
   CMFCPopupMenu* pMenuPopup,  
   CPane* pBar  
);  
```  
  
#### Parameters  
 [in] `pMenuPopup`  
 A pointer to a pop-up menu.  
  
 [in] `pBar`  
 A pointer to a tear-off bar.  
  
## Return Value  
 `TRUE` if the pop-up menu with the tear-off bar is enabled; otherwise `FALSE`.  
  
## Remarks  
 Override this method in a derived class to execute custom code when the framework displays a control bar.  
  
 The default implementation does nothing and returns `TRUE`.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)