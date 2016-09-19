---
title: "CMFCToolBarFontSizeComboBox::SetTwipSize"
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
ms.assetid: 99070ab3-ff6f-4ce5-8747-7a2b9f240189
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarFontSizeComboBox::SetTwipSize
Rounds the specified size (in twips) to the nearest size in points, and then sets the selected size in the combo box to that value.  
  
## Syntax  
  
```  
void SetTwipSize(  
   int nSize   
);  
```  
  
#### Parameters  
 [in] `nSize`  
 Specifies the font size (in twips) to set.  
  
## Remarks  
 You can retrieve the previous valid font size later by calling the [CMFCToolBarFontSizeComboBox::GetTwipSize](../vs140/CMFCToolBarFontSizeComboBox--GetTwipSize.md) method.  
  
## Requirements  
 **Header:** afxtoolbarfontcombobox.h  
  
## See Also  
 [CMFCToolBarFontSizeComboBox Class](../vs140/CMFCToolBarFontSizeComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)