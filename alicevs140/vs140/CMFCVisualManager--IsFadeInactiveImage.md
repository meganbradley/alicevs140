---
title: "CMFCVisualManager::IsFadeInactiveImage"
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
ms.assetid: 37205b88-9054-4b47-9250-d68360217ded
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::IsFadeInactiveImage
The framework calls this method when it draws inactive images on the toolbar or in a menu.  
  
## Syntax  
  
```  
BOOL IsFadeInactiveImage() const;  
```  
  
## Return Value  
 Nonzero if the framework uses the lighting effect when it draws inactive images on the toolbar or in a menu; otherwise 0.  
  
## Remarks  
 You can activate or deactivate the lighting effect by calling [CMFCVisualManager::SetFadeInactiveImage](../vs140/CMFCVisualManager--SetFadeInactiveImage.md). The lighting effect is what makes unavailable images appear faded.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCVisualManager::SetFadeInactiveImage](../vs140/CMFCVisualManager--SetFadeInactiveImage.md)