---
title: "CMFCFontComboBox::GetSelFont"
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
ms.assetid: d8dc66f3-398f-4c9b-bcfa-89995c581973
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFontComboBox::GetSelFont
Retrieves information about the currently selected font.  
  
## Syntax  
  
```  
CMFCFontInfo* GetSelFont() const;  
```  
  
## Return Value  
 A pointer to [CMFCFontInfo Class](../vs140/CMFCFontInfo-Class.md) object that describes a font. It can be `NULL` if no font is selected in the combo box.  
  
## Remarks  
  
## Requirements  
 **Header:** afxfontcombobox.h  
  
## See Also  
 [CMFCFontComboBox Class](../vs140/CMFCFontComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)