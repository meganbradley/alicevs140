---
title: "CMFCRibbonCategory::OnDrawMenuBorder"
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
ms.assetid: b8686104-b249-4235-b39c-ca54c3b3b402
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::OnDrawMenuBorder
Called by the framework to draw the border of a popup menu.  
  
## Syntax  
  
```  
virtual void OnDrawMenuBorder(  
    CDC* pDC,  
    CMFCRibbonPanelMenuBar* pMenuBar  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 This parameter is not used.  
  
 [in] `pMenuBar`  
 This parameter is not used.  
  
## Remarks  
 By default this method does nothing. Override this method to draw the border of a popup menu.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)