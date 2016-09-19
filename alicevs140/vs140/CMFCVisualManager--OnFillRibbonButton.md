---
title: "CMFCVisualManager::OnFillRibbonButton"
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
ms.assetid: 24340ab0-9008-41c3-9c1b-67f218f84cde
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillRibbonButton
The framework calls this method when it fills the interior of a ribbon button.  
  
## Syntax  
  
```  
virtual COLORREF OnFillRibbonButton(  
   CDC* pDC,  
   CMFCRibbonButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pButton`  
 A pointer to a [CMFCRibbonButton](../vs140/CMFCRibbonButton-Class.md) object. The framework fills the interior of this ribbon button.  
  
## Return Value  
 The color of text for the ribbon button specified by `pButton` if the ribbon button supports text. A value of -1 if text is invalid for the ribbon button.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of ribbon buttons.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)