---
title: "CMFCToolBarFontSizeComboBox::RebuildFontSizes"
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
ms.assetid: ea628c65-4775-4f67-933c-b06fe36aa1c0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarFontSizeComboBox::RebuildFontSizes
Fills a font size combo box with all valid sizes of the given font.  
  
## Syntax  
  
```  
void RebuildFontSizes(  
   const CString& strFontName   
);  
```  
  
#### Parameters  
 `[in] strFontName`  
 Specifies a font name.  
  
## Remarks  
 Call this function when you want to synchronize between selection in a font combo box and a font size combo box, such as a [CMFCToolBarFontComboBox](../vs140/CMFCToolBarFontComboBox-Class.md).  
  
## Requirements  
 **Header:** afxtoolbarfontcombobox.h  
  
## See Also  
 [CMFCToolBarFontSizeComboBox Class](../vs140/CMFCToolBarFontSizeComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)