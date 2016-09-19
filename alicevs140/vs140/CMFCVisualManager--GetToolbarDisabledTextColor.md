---
title: "CMFCVisualManager::GetToolbarDisabledTextColor"
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
ms.assetid: fff122ad-67f0-4f79-86d5-54160bbd3739
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::GetToolbarDisabledTextColor
The framework calls this function to determine the text color of toolbar buttons that are unavailable.  
  
## Syntax  
  
```  
virtual COLORREF GetToolbarDisabledTextColor();  
```  
  
## Return Value  
 The color that the framework uses for the text color of toolbar buttons that are unavailable.  
  
## Remarks  
 Override this method in a custom visual manager to set the text color of toolbar buttons that are unavailable .  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)