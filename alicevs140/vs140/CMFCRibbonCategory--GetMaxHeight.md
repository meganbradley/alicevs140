---
title: "CMFCRibbonCategory::GetMaxHeight"
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
ms.assetid: 2384a655-26f6-45dd-959b-0de6fa6ee35c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::GetMaxHeight
Retrieves the maximum height of the ribbon panels that are contained in the ribbon category.  
  
## Syntax  
  
```  
int GetMaxHeight(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context for the ribbon panels.  
  
## Return Value  
 The maximum height of the ribbon panels that are contained in the ribbon category.  
  
## Remarks  
 The value retrieved includes the height of the top and bottom margins for the ribbon panels.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)