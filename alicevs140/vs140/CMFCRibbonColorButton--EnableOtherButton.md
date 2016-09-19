---
title: "CMFCRibbonColorButton::EnableOtherButton"
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
ms.assetid: e9a146de-dafb-4d28-aa32-3380e5ce020f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonColorButton::EnableOtherButton
Enables the **Other** button.  
  
## Syntax  
  
```  
void EnableOtherButton(  
   LPCTSTR lpszLabel,  
   LPCTSTR lpszToolTip=NULL   
);  
```  
  
#### Parameters  
 `lpszLabel`  
 The button's label.  
  
 `lpszToolTip`  
 The tooltip text for the **Other** button.  
  
## Remarks  
 The **Other** button is the button that is displayed below the group of colors. When the user clicks the **Other** button, it displays a color dialog.  
  
## Requirements  
 **Header:** afxribboncolorbutton.h  
  
## See Also  
 [CMFCRibbonColorButton Class](../vs140/CMFCRibbonColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)