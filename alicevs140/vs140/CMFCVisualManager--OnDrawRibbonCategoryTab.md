---
title: "CMFCVisualManager::OnDrawRibbonCategoryTab"
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
ms.assetid: dd11e7e2-9cb3-4036-9408-3c2e7544be13
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonCategoryTab
The framework calls this method when it draws the tab for a ribbon category.  
  
## Syntax  
  
```  
virtual COLORREF OnDrawRibbonCategoryTab(  
   CDC* pDC,  
   CMFCRibbonTab* pTab,  
   BOOL bIsActive  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pTab`  
 A pointer to an instance of the `CMFCRibbonTab` class. The framework draws this tab.  
  
 [in] `bIsActive`  
 A Boolean parameter that indicates whether the tab is active.  
  
## Return Value  
 The color that is used for text on the ribbon category tab.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of a ribbon category tab. For more information about ribbon categories, see [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md).  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)