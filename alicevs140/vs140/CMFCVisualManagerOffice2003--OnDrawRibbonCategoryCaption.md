---
title: "CMFCVisualManagerOffice2003::OnDrawRibbonCategoryCaption"
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
ms.assetid: 24db8e4c-c2e4-46aa-8ebc-f13bbe754b63
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawRibbonCategoryCaption
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
 A pointer to the device context of the ribbon category.  
  
 [in] `pContextCaption`  
 A pointer to a caption bar. The visual manager draws this [CMFCRibbonContextCaption](../vs140/CMFCRibbonContextCaption-Class.md).  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter that indicates the color of the text on the caption bar.  
  
## Remarks  
 Override this method in a derived class to customize the appearance of the caption bar for a ribbon category.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)