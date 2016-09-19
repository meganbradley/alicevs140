---
title: "CMFCVisualManager::OnDrawRibbonMainPanelButtonBorder"
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
ms.assetid: aabf1155-8f6e-45fe-88fd-85e4cd11668d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonMainPanelButtonBorder
The framework calls this method when it draws the border of a [CMFCRibbonButton](../vs140/CMFCRibbonButton-Class.md) that is positioned on the **Main** panel.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonMainPanelButtonBorder(  
   CDC* pDC,  
   CMFCRibbonButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pButton`  
 A pointer to a `CMFCRibbonButton` located on the main panel of the ribbon. The framework draws the border for this button.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the border for a `CMFCRibbonButton` on the **Main** panel.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)