---
title: "CPaneFrameWnd::GetCaptionRect"
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
ms.assetid: 02f0055f-6761-4880-94dd-f74a769fca06
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::GetCaptionRect
Calculates the bounding rectangle of a mini-frame window caption.  
  
## Syntax  
  
```  
virtual void GetCaptionRect(  
    CRect& rectCaption  
) const;  
```  
  
#### Parameters  
 [out] `rectCaption`  
 Contains the size and position of the mini-frame window caption, in screen coordinates.  
  
## Remarks  
 This method is called by the framework to calculate the bounding rectangle of a mini-frame window caption.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)