---
title: "CMFCRibbonPanel::GetIndex"
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
ms.assetid: 4b7e7e45-d509-4602-88d8-85c62352cc66
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::GetIndex
Retrieves the zero-based index of the specified ribbon element from the array of ribbon elements that are contained in the ribbon panel.  
  
## Syntax  
  
```  
virtual int GetIndex(  
   CMFCRibbonBaseElement* pElem  
) const;  
```  
  
#### Parameters  
 [in] `pElem`  
 Pointer to a ribbon element.  
  
## Return Value  
 Zero-based index of the specified ribbon element if the method was successful; otherwise -1.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)