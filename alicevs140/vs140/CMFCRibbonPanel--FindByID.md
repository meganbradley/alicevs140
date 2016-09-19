---
title: "CMFCRibbonPanel::FindByID"
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
ms.assetid: 9c29ea9c-84f0-432a-bb80-6483e4d31e6e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::FindByID
Retrieves the ribbon element that is identified by the specified command ID.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* FindByID(  
    UINT uiCmdID   
) const;  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 The command ID of a ribbon element.  
  
## Return Value  
 The ribbon element that is identified by the specified command ID; otherwise `NULL` if no ribbon element is identified with the specified command ID.  
  
## Requirements  
 **Header:** afxRibbonPanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)