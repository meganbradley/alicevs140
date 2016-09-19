---
title: "CMFCRibbonColorButton::GetAutomaticColor"
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
ms.assetid: bc053737-f04c-4f77-8d1c-0168c6ee4929
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonColorButton::GetAutomaticColor
Retrieves the current automatic-button color.  
  
## Syntax  
  
```  
COLORREF GetAutomaticColor() const;  
```  
  
## Return Value  
 An RGB color value that represents the current automatic-button color.  
  
## Remarks  
 The automatic-button color is set by the `colorAutomatic` parameter passed to the `CMFCRibbonColorButton::EnableAutomaticButton` method.  
  
## Requirements  
 **Header:** afxribboncolorbutton.h  
  
## See Also  
 [CMFCRibbonColorButton Class](../vs140/CMFCRibbonColorButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)