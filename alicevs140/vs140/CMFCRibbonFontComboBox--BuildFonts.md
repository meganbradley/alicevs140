---
title: "CMFCRibbonFontComboBox::BuildFonts"
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
ms.assetid: f8144e5a-63f9-4bb3-b8ef-af6600610435
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonFontComboBox::BuildFonts
Populates the combo box on the ribbon with fonts.  
  
## Syntax  
  
```  
void BuildFonts(  
   int nFontType = DEVICE_FONTTYPE | RASTER_FONTTYPE | TRUETYPE_FONTTYPE,  
   BYTE nCharSet = DEFAULT_CHARSET,  
   BYTE nPitchAndFamily = DEFAULT_PITCH  
);  
```  
  
#### Parameters  
 [in] `nFontType`  
 Specifies the font type of the fonts to add.  
  
 [in] `nCharSet`  
 Specifies the character set of the fonts to add.  
  
 [in] `nPitchAndFamily`  
 Specifies the pitch and family of the fonts to add.  
  
## Requirements  
 **Header:** afxRibbonComboBox.h  
  
## See Also  
 [CMFCRibbonFontComboBox Class](../vs140/CMFCRibbonFontComboBox-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)