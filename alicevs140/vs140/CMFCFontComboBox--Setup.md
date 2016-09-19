---
title: "CMFCFontComboBox::Setup"
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
ms.assetid: 8e5cf7db-f3e9-4843-9eb2-470a47deeaa3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFontComboBox::Setup
Initializes the list of items in the font combo box.  
  
## Syntax  
  
```  
BOOL Setup(  
   int nFontType=DEVICE_FONTTYPE|RASTER_FONTTYPE|TRUETYPE_FONTTYPE,  
   BYTE nCharSet=DEFAULT_CHARSET,  
   BYTE nPitchAndFamily=DEFAULT_PITCH   
);  
```  
  
#### Parameters  
 [in] `nFontType`  
 Specifies the font type. The default value is the bitwise combination (OR) of DEVICE_FONTTYPE, RASTER_FONTTYPE, and TRUETYPE_FONTTYPE.  
  
 [in] `nCharSet`  
 Specifies the font character set. The default value is DEFAULT_CHARSET.  
  
 [in] `nPitchAndFamily`  
 Specifies the font pitch and family. The default value is DEFAULT_PITCH.  
  
## Return Value  
 `TRUE` if the font combo box was initialized successfully; otherwise, `FALSE`.  
  
## Remarks  
 This method initializes the font combo box by enumerating the currently installed fonts that match the specified parameters and inserting those font names in the font combo box.  
  
## Example  
 The following example demonstrates how to use the `Setup` method in the `CMFCFontComboBox` class. This example is part of the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#34](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#34)]  
[!CODE [NVC_MFC_NewControls#36](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#36)]  
  
## Requirements  
 **Header:** afxfontcombobox.h  
  
## See Also  
 [CMFCFontComboBox Class](../vs140/CMFCFontComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037)