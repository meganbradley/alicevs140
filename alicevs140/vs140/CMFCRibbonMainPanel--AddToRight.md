---
title: "CMFCRibbonMainPanel::AddToRight"
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
ms.assetid: 0392e771-16e4-4af4-900b-961a37e220fa
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonMainPanel::AddToRight
Adds a ribbon element to the right pane of the application button panel.  
  
## Syntax  
  
```  
void AddToRight(  
    CMFCRibbonBaseElement* pElem,  
    int nWidth = 300   
);  
```  
  
#### Parameters  
 `pElem`  
 A pointer to a ribbon element to be added to the right side of the main panel.  
  
 `nWidth`  
 Specifies the width, in pixels, of the right panel.  
  
## Remarks  
 Use this function to add a ribbon element to the right panel. The right panel typically displays the recent files list, but you can add any other ribbon element here.  
  
## Requirements  
 **Header:** afxRibbonMainPanel.h  
  
## See Also  
 [CMFCRibbonMainPanel Class](../vs140/CMFCRibbonMainPanel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)