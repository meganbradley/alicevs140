---
title: "CMFCRibbonBaseElement::GetKeyTipRect"
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
ms.assetid: 19ce240e-9387-4a04-9ea7-e4f9591a9f28
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::GetKeyTipRect
Retrieves the keytip boundary rectangle for the ribbon element.  
  
## Syntax  
  
```  
virtual CRect GetKeyTipRect(  
    CDC* pDC,  
    BOOL bIsMenu  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context.  
  
 [in] `bIsMenu`  
 `TRUE` if the ribbon element displays a pop-up menu; otherwise `FALSE`.  
  
## Return Value  
 Always returns a rectangle with 0 values.  
  
## Remarks  
 Override this method in a derived class to return the keytip boundary rectangle.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)