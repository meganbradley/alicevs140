---
title: "CMFCOutlookBarPane::IsBackgroundTexture"
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
ms.assetid: 0fe54ca3-0480-4dfe-a878-c2a5c5c2d966
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarPane::IsBackgroundTexture
Determines whether there is a background image loaded for the Outlook bar pane.  
  
## Syntax  
  
```  
BOOL IsBackgroundTexture() const;  
```  
  
## Return Value  
 `TRUE` if there is background image to display; otherwise `FALSE`.  
  
## Remarks  
 You can add a background image by calling [CMFCOutlookBarPane::SetBackImage](../vs140/CMFCOutlookBarPane--SetBackImage.md) function.  
  
 If there is no background image, the background is painted with a color specified by using [SetBackColor](../vs140/CMFCOutlookBarPane--SetBackColor.md).  
  
## Requirements  
 **Header:** afxoutlookbarpane.h  
  
## See Also  
 [CMFCOutlookBarPane Class](../vs140/CMFCOutlookBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)