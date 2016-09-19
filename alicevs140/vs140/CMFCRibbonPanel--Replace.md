---
title: "CMFCRibbonPanel::Replace"
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
ms.assetid: 42d85eee-af40-4582-a9ed-d3e1ea665dfa
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::Replace
Replaces one element with another based on their index value.  
  
## Syntax  
  
```  
BOOL Replace(  
    int nIndex,  
    CMFCRibbonBaseElement* pElem  
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the zero-based index of the element to replace.  
  
 [in] [out] `pElem`  
 A valid pointer to the element that replaces the original element.  
  
## Return Value  
 `TRUE` if the original ribbon element has been replaced successfully by the new ribbon element; `FALSE` if the ribbon element was not replaced or if there is no element at the specified index.  
  
## Remarks  
 To replace a ribbon element by command ID, call [CMFCRibbonPanel::ReplaceByID](../vs140/CMFCRibbonPanel--ReplaceByID.md).  
  
## Requirements  
 **Header:** afxRibbonPanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)