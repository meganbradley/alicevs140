---
title: "COleIPFrameWndEx::OnMenuButtonToolHitTest"
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
ms.assetid: 282bf76b-9e4d-4e9d-b596-a7dd59e8bbf4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::OnMenuButtonToolHitTest
Called by the framework when a [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md)object processes a `WM_NCHITTEST` message.  
  
## Syntax  
  
```  
virtual BOOL OnMenuButtonToolHitTest(  
   CMFCToolBarButton* pButton,  
   TOOLINFO* pTI   
);  
```  
  
#### Parameters  
 [in] pButton  
 Pointer to a menu button.  
  
 [out] pTI  
 Pointer to a `TOOLINFO` structure.  
  
## Return Value  
 The default implementation does nothing and returns 0. Your implementation should return a non-zero value if it fills the `pTI` parameter.  
  
## Remarks  
 Override this method to provide ToolTip information about a specific menu item.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)