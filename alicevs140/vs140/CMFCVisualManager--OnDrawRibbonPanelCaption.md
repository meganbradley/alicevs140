---
title: "CMFCVisualManager::OnDrawRibbonPanelCaption"
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
ms.assetid: 35808047-27b1-4340-9467-082bb2c2af17
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonPanelCaption
The framework calls this method when it draws the caption of a [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawRibbonPanelCaption(  
   CDC* pDC,  
   CMFCRibbonPanel* pPanel,  
   CRect rectCaption  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pPanel`  
 A pointer to a `CMFCRibbonPanel` object. The framework draws the caption for this ribbon panel.  
  
 [in] `rectCaption`  
 A rectangle that specifies the boundaries of the caption for the ribbon panel.  
  
## Remarks  
 Override this method in a derived class to customize the appearance of captions for ribbon panels.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)