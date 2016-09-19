---
title: "CMFCRibbonBaseElement::SetParentCategory"
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
ms.assetid: 201efaf7-05c3-438d-b58a-ee08b647eac1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::SetParentCategory
Sets the parent category for the ribbon element.  
  
## Syntax  
  
```  
virtual void SetParentCategory(  
   CMFCRibbonCategory* pParent  
);  
```  
  
#### Parameters  
 [in] `pParent`  
 Pointer to a ribbon category.  
  
## Remarks  
 The tabbed groups in ribbon controls are called categories.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)