---
title: "CMFCRibbonBaseElement::SetOriginal"
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
ms.assetid: 1ff65b30-d6f2-474d-b2d0-4bb37e686931
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::SetOriginal
Sets the original ribbon element for the ribbon element.  
  
## Syntax  
  
```  
virtual void SetOriginal(  
   CMFCRibbonBaseElement* pOriginal  
);  
```  
  
#### Parameters  
 [in] `pOriginal`  
 Pointer to a ribbon element.  
  
## Remarks  
 Ribbon elements that are copied to another container retain a pointer to the original ribbon element.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)