---
title: "CMFCColorButton::EnableAutomaticButton"
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
ms.assetid: 219a4dd3-25f7-421d-8470-924444d60cff
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::EnableAutomaticButton
Enable or disable the "automatic" button of a color picker control and set the automatic (default) color.  
  
## Syntax  
  
```  
void EnableAutomaticButton(  
   LPCTSTR lpszLabel,  
   COLORREF colorAutomatic,  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 Specifies the automatic button's text.  
  
 [in] `colorAutomatic`  
 An RGB value that specifies the automatic button's default color.  
  
 [in] `bEnable`  
 Specifies whether the automatic button is enabled or disabled.  
  
## Remarks  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)