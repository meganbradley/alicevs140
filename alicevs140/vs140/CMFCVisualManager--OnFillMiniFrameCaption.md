---
title: "CMFCVisualManager::OnFillMiniFrameCaption"
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
ms.assetid: b983486f-16ba-4f2b-94aa-dd746dda592c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillMiniFrameCaption
The framework calls this method when it fills the caption bar of a mini frame window.  
  
## Syntax  
  
```  
virtual COLORREF OnFillMiniFrameCaption(  
   CDC* pDC,  
   CRect rectCaption,  
   CPaneFrameWnd* pFrameWnd,  
   BOOL bActive  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectCaption`  
 A rectangle that specifies the boundaries of the caption bar.  
  
 [in] `pFrameWnd`  
 A pointer to a mini frame window. The framework draws the caption bar for this window.  
  
 [in] `bActive`  
 A Boolean parameter that indicates if the window is active.  
  
## Return Value  
 The color that is used to fill the background of the caption bar.  
  
## Remarks  
 The default implementation for this method fills the caption bar with the current caption color for the active skin.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)