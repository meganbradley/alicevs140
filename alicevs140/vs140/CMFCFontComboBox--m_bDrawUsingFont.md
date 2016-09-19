---
title: "CMFCFontComboBox::m_bDrawUsingFont"
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
ms.assetid: f4a30a4f-51bb-4495-9621-5be4bcf326e0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFontComboBox::m_bDrawUsingFont
Indicates to the framework which font to use to draw the item labels in the current font combo box.  
  
## Syntax  
  
```  
static BOOL m_bDrawUsingFont;  
```  
  
## Remarks  
 Set this member to `TRUE` to direct the framework to use the same font to draw each item label. Set this member to `FALSE` to direct the framework to draw each item label with the font whose name is the same as the label. The default value of this member is `FALSE`.  
  
## Requirements  
 **Header:** afxfontcombobox.h  
  
## See Also  
 [CMFCFontComboBox Class](../vs140/CMFCFontComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)