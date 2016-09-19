---
title: "CMFCRibbonFontComboBox::SetFont"
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
ms.assetid: 91fe000e-6fca-4e02-81dc-ae0d188ad4bb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonFontComboBox::SetFont
Selects the specified font in the combo box.  
  
## Syntax  
  
```  
BOOL SetFont(  
    LPCTSTR lpszName,  
    BYTE nCharSet = DEFAULT_CHARSET,  
    BOOL bExact = FALSE   
);  
```  
  
#### Parameters  
 `lpszName`  
 Specifies the name of the font to select.  
  
 `nCharSet`  
 Specifies the character set for the selected font.  
  
 `bExact`  
 `TRUE` to specify that the character set must match when selecting a font; `FALSE` to specify that the character set can be ignored when selecting a font.  
  
## Return Value  
 Nonzero if the specified font was found and selected; otherwise, zero.  
  
## Remarks  
  
## Requirements  
 **Header:** afxRibbonComboBox.h  
  
## See Also  
 [CMFCRibbonFontComboBox Class](../vs140/CMFCRibbonFontComboBox-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)