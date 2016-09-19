---
title: "CMFCRibbonCategory::GetElements"
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
ms.assetid: 94f6b4d0-1b18-4127-8005-8f1a38435151
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::GetElements
Retrieves all ribbon elements in the ribbon category.  
  
## Syntax  
  
```  
void GetElements(  
   CArray <CMFCRibbonBaseElement*, CMFCRibbonBaseElement*>& arElements  
);  
```  
  
#### Parameters  
 [in, out] `arElements`  
 Reference to a [CArray](../vs140/CArray-Class.md) of ribbon elements.  
  
## Remarks  
 Ribbon elements that are designed for use on the quick access toolbar are included in the array.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)