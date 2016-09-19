---
title: "CMFCRibbonBaseElement::HitTest"
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
ms.assetid: 91766536-593f-4fed-976b-1b6abb201d43
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::HitTest
Retrieves a pointer to the ribbon element if the specified point is located in it.  
  
## Syntax  
  
```  
virtual CMFCRibbonBaseElement* HitTest(  
   CPoint point  
);  
```  
  
#### Parameters  
 [in] `point`  
 This parameter is not used.  
  
## Return Value  
 A pointer to the ribbon element if it exists; otherwise `FALSE`.  
  
## Remarks  
 By default this method always returns a valid pointer to the ribbon element when it exists. Override this method to indicate if the point resides in the ribbon element.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)