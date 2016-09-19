---
title: "CMFCStatusBar::SetPaneAnimation"
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
ms.assetid: c82fd8e3-1c8e-4f1c-b94b-ebcbe24337ac
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCStatusBar::SetPaneAnimation
Assigns an animation to the specified pane.  
  
## Syntax  
  
```  
void SetPaneAnimation(  
   int nIndex,  
   HIMAGELIST hImageList,  
   UINT nFrameRate=500,  
   BOOL bUpdate=TRUE   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of the pane to which you want to assign to it an animation.  
  
 [in] `hImageList`  
 Specifies a handle to the image list that holds the animation frames.  
  
 [in] `nFrameRate`  
 Specifies the frame rate, in milliseconds, for the animation.  
  
 [in] `bUpdate`  
 If `TRUE`, update the pane content immediately. Otherwise, the pane content is updated when it is invalidated.  
  
## Remarks  
 If you want to disable the current animation, call `SetPaneAnimation` with `hImageList` set to `NULL`.  
  
## Requirements  
 **Header:** afxstatusbar.h  
  
## See Also  
 [CMFCStatusBar Class](../vs140/CMFCStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)