---
title: "CMFCVisualManager::OnDrawRibbonLabel"
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
ms.assetid: 737a1979-cc94-4a28-8d02-51278382f5c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonLabel
The framework calls this method when it draws the label of the ribbon.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonLabel(  
   CDC* pDC,  
   CMFCRibbonLabel* pLabel,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pLabel`  
 A pointer to a [CMFCRibbonLabel](../vs140/CMFCRibbonLabel-Class.md) object. The framework draws this ribbon label.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the ribbon panel.  
  
## Remarks  
 Override this method in a derived class to customize the ribbon label.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonLabel Class](../vs140/CMFCRibbonLabel-Class.md)