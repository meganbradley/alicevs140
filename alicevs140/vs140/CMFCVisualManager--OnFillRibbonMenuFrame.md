---
title: "CMFCVisualManager::OnFillRibbonMenuFrame"
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
ms.assetid: 6853be03-f6e0-4c46-8710-ce708f78869c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillRibbonMenuFrame
The framework calls this method when it fills the menu frame of the ribbon panel.  
  
## Syntax  
  
```  
virtual void OnFillRibbonMenuFrame(  
   CDC* pDC,  
   CMFCRibbonMainPanel* pPanel,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pPanel`  
 A pointer to an instance of the [CMFCRibbonMainPanel Class](../vs140/CMFCRibbonMainPanel-Class.md). The framework fills the menu frame for this ribbon panel.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the menu frame.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the menu bar for the `CMFCRibbonMainPanel`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonMainPanel Class](../vs140/CMFCRibbonMainPanel-Class.md)