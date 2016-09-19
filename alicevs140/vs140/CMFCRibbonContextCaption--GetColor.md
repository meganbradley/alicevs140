---
title: "CMFCRibbonContextCaption::GetColor"
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
ms.assetid: f2406fc4-c2dc-41c0-8ad6-5559db4b4b18
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonContextCaption::GetColor
Returns the background color of the caption.  
  
## Syntax  
  
```  
AFX_RibbonCategoryColor GetColor() const;  
```  
  
## Return Value  
 The returned value can be one of the following enumerated values:  
  
-   `AFX_CategoryColor_None`  
  
-   `AFX_CategoryColor_Red`  
  
-   `AFX_CategoryColor_Orange`  
  
-   `AFX_CategoryColor_Yellow`  
  
-   `AFX_CategoryColor_Green`  
  
-   `AFX_CategoryColor_Blue`  
  
-   `AFX_CategoryColor_Indigo`  
  
-   `AFX_CategoryColor_Violet`  
  
## Remarks  
 The color of the caption can be set by calling [CMFCRibbonCategory::SetTabColor](../vs140/CMFCRibbonCategory--SetTabColor.md) or [CMFCRibbonBar::AddContextCategory](../vs140/CMFCRibbonBar--AddContextCategory.md).  
  
## Requirements  
 **Header:** afxRibbonBar.h  
  
## See Also  
 [CMFCRibbonContextCaption Class](../vs140/CMFCRibbonContextCaption-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)