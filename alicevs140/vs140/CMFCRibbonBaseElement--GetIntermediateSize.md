---
title: "CMFCRibbonBaseElement::GetIntermediateSize"
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
ms.assetid: 17e13c6b-6052-4f2d-90e1-e183bcff4a8e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::GetIntermediateSize
Returns the size of the ribbon element in its intermediate state.  
  
## Syntax  
  
```  
virtual CSize GetIntermediateSize(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
## Return Value  
 The size of the ribbon element in its intermediate state.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)