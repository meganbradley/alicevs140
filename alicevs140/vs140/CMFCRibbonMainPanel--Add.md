---
title: "CMFCRibbonMainPanel::Add"
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
ms.assetid: 395d676c-33fc-42e4-9082-f4cc904251c7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonMainPanel::Add
Adds a ribbon element to the left pane of the application button panel.  
  
## Syntax  
  
```  
virtual void Add(  
    CMFCRibbonBaseElement* pElem   
);  
```  
  
#### Parameters  
 [in] [out] `pElem`  
 A pointer to the ribbon element to add to the main panel.  
  
## Remarks  
 Adds a ribbon element to the panel. Elements added using this method will be located in the left column of the main panel.  
  
## Requirements  
 **Header:** afxRibbonMainPanel.h  
  
## See Also  
 [CMFCRibbonMainPanel Class](../vs140/CMFCRibbonMainPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)