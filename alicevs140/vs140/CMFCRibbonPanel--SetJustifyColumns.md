---
title: "CMFCRibbonPanel::SetJustifyColumns"
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
ms.assetid: 347decfa-e9bf-4b1d-be0a-8982d1fa964f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::SetJustifyColumns
Enables or disables the adjustment of the width of ribbon elements in the same column.  
  
## Syntax  
  
```  
void SetJustifyColumns(  
    BOOL bSet = TRUE  
);  
```  
  
#### Parameters  
 [in] `bSet`  
 `TRUE` to adjust the width of ribbon elements in the same column to the width of the largest ribbon element in the column; `FALSE` to disable this width adjustment.  
  
## Remarks  
 When this feature is enabled in a ribbon panel, the widths of ribbon elements in the same column are adjusted to the width of the largest ribbon element in the same column.  
  
## Requirements  
 **Header:** afxRibbonPanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)