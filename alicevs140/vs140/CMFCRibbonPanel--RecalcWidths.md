---
title: "CMFCRibbonPanel::RecalcWidths"
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
ms.assetid: 138faa21-e96a-4fbe-9575-0ba5eaf0017e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::RecalcWidths
Recalculates the width of each display layout configuration for the ribbon panel.  
  
## Syntax  
  
```  
virtual void RecalcWidths(  
   CDC* pDC,  
   int nHeight  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context for the ribbon panel.  
  
 [in] `nHeight`  
 The height of the ribbon panel.  
  
## Remarks  
 A ribbon panel changes its layout configuration as the available width changes.  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)