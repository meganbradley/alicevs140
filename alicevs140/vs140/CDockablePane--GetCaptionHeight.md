---
title: "CDockablePane::GetCaptionHeight"
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
ms.assetid: 678fb380-9f8a-4cb9-bce1-cad348380db9
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::GetCaptionHeight
Returns the height, in pixels, of the current caption.  
  
## Syntax  
  
```  
virtual int GetCaptionHeight() const;  
```  
  
## Return Value  
 The height of the caption, in pixels.  
  
## Remarks  
 The caption height is 0 if the caption was hidden by the [CDockablePane::EnableGripper](../vs140/CDockablePane--EnableGripper.md) method, or if the pane does not have a caption.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)