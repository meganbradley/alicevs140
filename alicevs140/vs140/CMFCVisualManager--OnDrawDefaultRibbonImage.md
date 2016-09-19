---
title: "CMFCVisualManager::OnDrawDefaultRibbonImage"
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
ms.assetid: 29a72b2e-fadc-42e1-936d-7b04ef56b964
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawDefaultRibbonImage
The framework calls this method when it draws the default image that is used for the ribbon button.  
  
## Syntax  
  
```  
virtual void OnDrawDefaultRibbonImage(  
   CDC* pDC,  
   CRect rectImage,  
   BOOL bIsDisabled = FALSE,  
   BOOL bIsPressed = FALSE,  
   BOOL bIsHighlighted = FALSE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectImage`  
 A rectangle that specifies the boundaries of the default image.  
  
 [in] `bIsDisabled`  
 A Boolean parameter that indicates whether the ribbon button is unavailable.  
  
 [in] `bIsPressed`  
 A Boolean parameter that indicates whether the ribbon button is pressed.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the ribbon button is highlighted.  
  
## Remarks  
 Override this method in a derived visual manager if you want to customize the image that is used for the ribbon button.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)