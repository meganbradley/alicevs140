---
title: "CMFCRibbonBaseElement::OnChangeMenuHighlight"
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
ms.assetid: 853f65de-4c9e-47d8-a8a2-f98eb26851d5
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::OnChangeMenuHighlight
Called by the framework when the highlight changes for a ribbon element that is located in a menu.  
  
## Syntax  
  
```  
virtual void OnChangeMenuHighlight(  
   CMFCRibbonPanelMenuBar* pPanelMenuBar  
   CMFCRibbonBaseElement* pHot  
);  
```  
  
#### Parameters  
 [in] `pPanelMenuBar`  
 This parameter is not used.  
  
 [in] `pHot`  
 This parameter is not used.  
  
## Remarks  
 By default this method does nothing. Override this method to update a ribbon element that is located in a menu when the highlight changes.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)