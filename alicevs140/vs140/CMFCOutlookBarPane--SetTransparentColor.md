---
title: "CMFCOutlookBarPane::SetTransparentColor"
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
ms.assetid: ba8c9599-fc67-4a5e-8af8-27e15371eaaf
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarPane::SetTransparentColor
Sets the transparent color for the Outlook bar pane.  
  
## Syntax  
  
```  
void SetTransparentColor(  
   COLORREF color   
);  
```  
  
#### Parameters  
 `color`  
 Specifies the new transparent color.  
  
## Remarks  
 The transparent color is required to display transparent images. Any occurrence of this color in an image is painted with the background color instead.  There is no blending of background and foreground images.  
  
## Requirements  
 **Header:** afxoutlookbarpane.h  
  
## See Also  
 [CMFCOutlookBarPane Class](../vs140/CMFCOutlookBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)