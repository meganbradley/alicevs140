---
title: "CFrameWndEx::OnDrawMenuLogo"
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
ms.assetid: 62789935-0664-4db8-8c52-3f4442454e80
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnDrawMenuLogo
Called by the framework when a `CMFCPopupMenu` object processes a WM_PAINT message.  
  
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
 A pointer to a device context.  
  
 [in] `pMenu`  
 A pointer to the menu item.  
  
 [in] `rectLogo`  
 A reference to a constant `CRect` structure that specifies the screen position and size of the menu logo.  
  
## Remarks  
 Override this function if you want to display a logo on the pop-up menu that belongs to the menu bar owned by the `CFrameWndEx` derived object.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)