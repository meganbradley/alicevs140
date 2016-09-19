---
title: "CMFCRibbonCategory::GetPanel"
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
ms.assetid: 6f96ce56-22a1-4aac-92c3-a172a3ece948
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::GetPanel
Returns a pointer to the ribbon panel that is located at the specified index.  
  
## Syntax  
  
```  
CMFCRibbonPanel* GetPanel(  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index of a ribbon panel.  
  
## Return Value  
 Pointer to the ribbon panel that is located at the specified index.  
  
## Remarks  
 An exception is thrown if `nIndex` is out of range.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)