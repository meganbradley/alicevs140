---
title: "COleIPFrameWndEx::OnDrawMenuLogo"
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
ms.assetid: 3b7bda5e-3741-46a6-96ce-38e7ce21dc0c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::OnDrawMenuLogo
Called by the framework when a [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md)object processes a `WM_PAINT` message.  
  
## Syntax  
  
```  
virtual void OnDrawMenuLogo(  
   CDC* pDC,  
   CMFCPopupMenu* pMenu,  
   const CRect& rectLogo   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the device context.  
  
 [in] `pMenu`  
 Pointer to the pop-up menu object.  
  
 [in] `rectLogo`  
 Pointer to the logo to display.  
  
## Remarks  
 Override this method to display a logo on the pop-up menu associated with the menu bar owned by the `COleIPFrameWndEx`-derived object. The default implementation does nothing.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)