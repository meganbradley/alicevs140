---
title: "COleIPFrameWndEx::OnDrawMenuImage"
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
ms.assetid: aaec10a5-5e66-4b1b-a4a4-3e0c55c14fcc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::OnDrawMenuImage
Called by the framework when the image that is associated with a menu item is drawn.  
  
## Syntax  
  
```  
virtual BOOL OnDrawMenuImage(  
   CDC* pDC,  
   const CMFCToolBarMenuButton* pMenuButton,  
   const CRect& rectImage   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the device context.  
  
 [in] `pMenuButton`  
 Pointer to the menu button.  
  
 [in] `rectImage`  
 The image associated with the menu item.  
  
## Return Value  
 The default implementation does nothing and returns 0.  
  
## Remarks  
 Override this method if you want to customize image drawing for the menu items that belong to the menu bar owned by the `COleIPFrameWndEx`-derived object.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)