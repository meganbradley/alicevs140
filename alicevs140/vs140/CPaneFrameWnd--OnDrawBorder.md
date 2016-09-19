---
title: "CPaneFrameWnd::OnDrawBorder"
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
ms.assetid: 21c18af9-a6d7-4b82-baad-7bf6c5bceef0
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::OnDrawBorder
Draws the borders of a mini-frame window.  
  
## Syntax  
  
```  
virtual void OnDrawBorder(  
    CDC* pDC   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 The device context used to draw the border.  
  
## Remarks  
 This method is called by the framework to draw the borders of the mini-frame window.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)