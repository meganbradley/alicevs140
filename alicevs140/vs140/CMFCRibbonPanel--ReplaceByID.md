---
title: "CMFCRibbonPanel::ReplaceByID"
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
ms.assetid: 4072e987-238c-41a6-8355-c00e71c6e1f8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::ReplaceByID
Replaces one element with another based on a specified command ID.  
  
## Syntax  
  
```  
BOOL ReplaceByID(  
    UINT uiCmdID,  
    CMFCRibbonBaseElement* pElem   
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 Specifies the command ID of the element to replace.  
  
 [in] [out] `pElem`  
 A valid pointer to the element that will replace the original element.  
  
## Return Value  
 `TRUE` if the original ribbon element has been replaced successfully by the new ribbon element; `FALSE` if the ribbon element was not replaced or if no element with the specified command ID actually exists.  
  
## Remarks  
 To replace a ribbon element based on position, call [CMFCRibbonPanel::Replace](../vs140/CMFCRibbonPanel--Replace.md).  
  
## Requirements  
 **Header:** afxRibbonPanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)