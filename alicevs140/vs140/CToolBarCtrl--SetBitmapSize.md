---
title: "CToolBarCtrl::SetBitmapSize"
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
ms.assetid: a315d565-a69d-4b80-99c1-71779edbe52c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetBitmapSize
Sets the size of the actual bitmapped images to be added to a toolbar control.  
  
## Syntax  
  
```  
  
      BOOL SetBitmapSize(  
   CSize size   
);  
```  
  
#### Parameters  
 `size`  
 Width and height, in pixels, of the bitmapped images.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This function must be called only before adding any bitmaps to the toolbar. If the application does not explicitly set the bitmap size, it defaults to 16 by 15 pixels.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetButtonSize](../vs140/CToolBarCtrl--SetButtonSize.md)   
 [CToolBarCtrl::GetItemRect](../vs140/CToolBarCtrl--GetItemRect.md)