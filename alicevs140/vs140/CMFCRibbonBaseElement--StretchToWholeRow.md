---
title: "CMFCRibbonBaseElement::StretchToWholeRow"
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
ms.assetid: f26dcdb3-b0dc-46e2-8509-3a1a12024c40
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::StretchToWholeRow
Changes the display height of the ribbon element to the specified row height.  
  
## Syntax  
  
```  
virtual BOOL StretchToWholeRow(  
   CDC* pDC,  
   int nHeight  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 This parameter is not used.  
  
 [in] `nHeight`  
 The height of the row.  
  
## Return Value  
 `TRUE` if the display height was set; otherwise, `FALSE`.  
  
## Remarks  
 Override this method to change the display height of the ribbon element to the specified row height.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)