---
title: "CMFCColorBar::GetExtraHeight"
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
ms.assetid: 038c2072-4217-48e8-b11c-7f2f590b9971
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::GetExtraHeight
Calculates the additional height that the current color bar requires to display miscellaneous user interface elements, such as the **Other** button or document colors.  
  
## Syntax  
  
```  
int GetExtraHeight(  
   int nNumColumns  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nNumColumns`|If the color bar control contains document colors, the number of columns to display in the grid of document colors. Otherwise, this value is not used.|  
  
## Return Value  
 The calculated extra height that is required.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [CMFCColorBar::EnableAutomaticButton](../vs140/CMFCColorBar--EnableAutomaticButton.md)   
 [CMFCColorBar::EnableOtherButton](../vs140/CMFCColorBar--EnableOtherButton.md)   
 [CMFCColorBar::SetDocumentColors](../vs140/CMFCColorBar--SetDocumentColors.md)