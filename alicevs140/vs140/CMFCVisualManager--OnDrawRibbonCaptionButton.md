---
title: "CMFCVisualManager::OnDrawRibbonCaptionButton"
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
ms.assetid: 35396537-fa89-4f11-bda7-c221b2cc86dc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonCaptionButton
The framework calls this method when it draws a caption button located on the ribbon bar.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonCaptionButton(  
   CDC* pDC,  
   CMFCRibbonCaptionButton* pButton  
);  
```  
  
#### Parameters  
 `pDC`  
 A pointer to a device context.  
  
 `pButton`  
 A pointer to a `CMFCRibbonCaptionButton` class. The framework draws this caption button.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of a caption button on the ribbon.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)