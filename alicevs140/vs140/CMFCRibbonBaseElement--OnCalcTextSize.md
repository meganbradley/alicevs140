---
title: "CMFCRibbonBaseElement::OnCalcTextSize"
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
ms.assetid: b8b621a1-c4eb-4ac8-956e-a5cbb7a3ab26
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::OnCalcTextSize
Calculates the size of the text for the ribbon element.  
  
## Syntax  
  
```  
virtual void OnCalcTextSize(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 This parameter is not used.  
  
## Remarks  
 By default this method does nothing. Override this method to calculate the size of the text for the ribbon element.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)