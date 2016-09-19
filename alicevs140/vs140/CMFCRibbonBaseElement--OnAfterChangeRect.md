---
title: "CMFCRibbonBaseElement::OnAfterChangeRect"
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
ms.assetid: d7a2d392-fc80-45f6-91af-78cff0d9cac9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::OnAfterChangeRect
Updates the tooltip for the ribbon element.  
  
## Syntax  
  
```  
virtual void OnAfterChangeRect(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 This parameter is not used.  
  
## Remarks  
 By default this method updates the tooltip for the ribbon element. Override this method to update the ribbon element after its display rectangle has changed.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)