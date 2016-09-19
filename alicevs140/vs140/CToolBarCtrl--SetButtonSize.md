---
title: "CToolBarCtrl::SetButtonSize"
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
ms.assetid: cf57d423-f7fe-496e-8514-f9fc31d3c426
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetButtonSize
Sets the size of the buttons in the toolbar control.  
  
## Syntax  
  
```  
  
      BOOL SetButtonSize(  
   CSize size   
);  
```  
  
#### Parameters  
 `size`  
 Width and height, in pixels, of the buttons.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The button size must always be at least as large as the bitmap size it encloses. This function must be called only before adding any bitmaps to the toolbar. If the application does not explicitly set the button size, it defaults to 24 by 22 pixels.  
  
## Example  
 See the example for [CToolBar::GetToolBarCtrl](../vs140/CToolBar--GetToolBarCtrl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetBitmapSize](../vs140/CToolBarCtrl--SetBitmapSize.md)   
 [CToolBarCtrl::GetItemRect](../vs140/CToolBarCtrl--GetItemRect.md)