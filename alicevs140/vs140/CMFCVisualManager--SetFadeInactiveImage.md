---
title: "CMFCVisualManager::SetFadeInactiveImage"
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
ms.assetid: aa97ba7c-4729-4b9c-9fcf-d83e229687a3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::SetFadeInactiveImage
Enables or disables the lighting effect for inactive images on a menu or toolbar.  
  
## Syntax  
  
```  
void SetFadeInactiveImage(  
   BOOL bFade = TRUE  
);  
```  
  
#### Parameters  
 [in] `bFade`  
 A Boolean parameter that specifies whether to enable the lighting effect.  
  
## Remarks  
 This feature controls whether inactive images appear faded on a menu or toolbar. Use the method [CMFCVisualManager::IsFadeInactiveImage](../vs140/CMFCVisualManager--IsFadeInactiveImage.md) to determine whether this feature is enabled.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCVisualManager::IsFadeInactiveImage](../vs140/CMFCVisualManager--IsFadeInactiveImage.md)