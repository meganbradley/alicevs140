---
title: "CMFCPopupMenu::EnableMenuLogo"
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
ms.assetid: 3e11d97f-c098-404e-abdf-be1a5a1f1e70
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::EnableMenuLogo
Initializes the logo for a pop-up menu.  
  
## Syntax  
  
```  
void EnableMenuLogo(  
   int iLogoSize,  
   LOGO_LOCATION nLogoLocation = MENU_LOGO_LEFT  
);  
```  
  
#### Parameters  
 [in] `iLogoSize`  
 The size of the logo, in pixels.  
  
 [in] `nLogoLocation`  
 An enumerated data type that indicates the location of the logo.  
  
## Remarks  
 To display the logo, implement the method [CFrameWndEx::OnDrawMenuLogo](../vs140/CFrameWndEx--OnDrawMenuLogo.md) in the main frame window.  
  
 The possible values for `nLogoLocation` are MENU_LOGO_LEFT, MENU_LOGO_RIGHT, MENU_LOGO_TOP, and MENU_LOGO_BOTTOM.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CFrameWndEx::OnDrawMenuLogo](../vs140/CFrameWndEx--OnDrawMenuLogo.md)