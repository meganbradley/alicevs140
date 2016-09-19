---
title: "CMFCVisualManager::OnDrawRibbonCategoryCaption"
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
ms.assetid: 0ef3fc40-2410-4bf7-a651-16f94b012fc4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonCategoryCaption
The framework calls this method when it draws the caption bar for a ribbon category.  
  
## Syntax  
  
```  
virtual COLORREF OnDrawRibbonCategoryCaption(  
   CDC* pDC,  
   CMFCRibbonContextCaption* pContextCaption  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 The drawing context.  
  
 [in] `pContextCaption`  
 A pointer to a caption bar. The visual manager draws this [CMFCRibbonContextCaption Class](../vs140/CMFCRibbonContextCaption-Class.md) object.  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter that indicates the color of the text on the caption bar.  
  
## Remarks  
 Override this method in a derived class to customize the appearance of the caption bar for a ribbon category. For more information about the caption bar, see [CMFCRibbonContextCaption Class](../vs140/CMFCRibbonContextCaption-Class.md).  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonContextCaption Class](../vs140/CMFCRibbonContextCaption-Class.md)