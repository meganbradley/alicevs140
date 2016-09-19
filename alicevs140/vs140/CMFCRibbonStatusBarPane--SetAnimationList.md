---
title: "CMFCRibbonStatusBarPane::SetAnimationList"
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
ms.assetid: 91b56cf3-e198-49fe-9765-b8057cc9db7f
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBarPane::SetAnimationList
Attaches to the status bar pane an image list that can be used for animation.  
  
## Syntax  
  
```  
void SetAnimationList(  
   HBITMAP hBmpAnimationList,  
   int cxAnimation=16,  
   COLORREF clrTransp=RGB(192,  
   192 1,  
   192) 1   
);  
BOOL SetAnimationList(  
   UINT uiAnimationListResID,  
   int cxAnimation=16,  
   COLORREF clrTransp=RGB(192,  
   192 1,  
   192) 1   
);  
```  
  
#### Parameters  
 [in] `hBmpAnimationList`  
 Specifies a handle to an image list.  
  
 [in] `cxAnimation`  
 Specifies the width, in pixels, of the frame in the image list.  
  
 [in] `clrTransp`  
 Specifies the transparent color of the image list.  
  
 [in] `uiAnimationListResID`  
 Specifies the resource ID of the image list.  
  
## Return Value  
 `TRUE` if the image list is successfully attached to the status bar pane; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxribbonstatusbarpane.h  
  
## See Also  
 [CMFCRibbonStatusBarPane Class](../vs140/CMFCRibbonStatusBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)