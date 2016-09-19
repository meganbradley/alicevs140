---
title: "CMFCRibbonPanel::HasElement"
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
ms.assetid: ef84b9f3-4451-4bac-aa62-3ded2eb52b78
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::HasElement
Indicates whether the ribbon panel contains the specified ribbon element.  
  
## Syntax  
  
```  
BOOL HasElement(  
   const CMFCRibbonBaseElement* pElem  
) const;  
```  
  
#### Parameters  
 [in] `pElem`  
 Pointer to a ribbon element.  
  
## Return Value  
 `TRUE` if the ribbon panel contains the specified ribbon element; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)