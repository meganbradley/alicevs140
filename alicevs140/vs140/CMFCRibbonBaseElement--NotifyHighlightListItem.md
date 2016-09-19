---
title: "CMFCRibbonBaseElement::NotifyHighlightListItem"
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
ms.assetid: 16912f7b-5f4c-49cd-99ee-5a358788d791
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::NotifyHighlightListItem
Notifies the parent window of the ribbon bar when a user highlights a ribbon element that is located in a list.  
  
## Syntax  
  
```  
virtual void NotifyHighlightListItem(  
   int nIndex  
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The index of the ribbon element in the list.  
  
## Remarks  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)