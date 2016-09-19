---
title: "CMFCVisualManager::IsEmbossDisabledImage"
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
ms.assetid: d2b297a1-759e-411d-b8c3-6d1a15ffdd60
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::IsEmbossDisabledImage
Specifies whether the framework embosses images that are unavailable.  
  
## Syntax  
  
```  
BOOL IsEmbossDisabledImage() const;  
```  
  
## Return Value  
 Nonzero if the framework embosses images that are unavailable; otherwise 0.  
  
## Remarks  
 This method is called by [CMFCToolBarImages::Draw](../vs140/CMFCToolBarImages--Draw.md) when it draws an image on the toolbar that is unavailable.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCVisualManager::SetEmbossDisabledImage](../vs140/CMFCVisualManager--SetEmbossDisabledImage.md)