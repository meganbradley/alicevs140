---
title: "CDC::RectVisible"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: d2935997-9948-476e-a682-d193e83597de
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::RectVisible
Determines whether any part of the given rectangle lies within the clipping region of the display context.  
  
## Syntax  
  
```  
  
      virtual BOOL RectVisible(  
   LPCRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpRect`  
 Points to a `RECT` structure or a `CRect` object that contains the logical coordinates of the specified rectangle.  
  
## Return Value  
 Nonzero if any portion of the given rectangle lies within the clipping region; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::PtVisible](../vs140/CDC--PtVisible.md)   
 [CDC::SelectClipRgn](../vs140/CDC--SelectClipRgn.md)   
 [CRect Class](../vs140/CRect-Class.md)   
 [RectVisible](http://msdn.microsoft.com/library/windows/desktop/dd162908)   
 [RECT Structure](../vs140/RECT-Structure.md)