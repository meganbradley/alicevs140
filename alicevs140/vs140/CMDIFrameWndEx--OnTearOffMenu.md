---
title: "CMDIFrameWndEx::OnTearOffMenu"
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
ms.assetid: 1bdae8fe-c166-4618-96b6-281d2c076769
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnTearOffMenu
Called by the framework when a menu that has a tear-off bar is activated.  
  
## Syntax  
  
```  
virtual BOOL OnTearOffMenu(  
   CMFCPopupMenu* pMenuPopup,  
   CPane* pBar  
);  
```  
  
#### Parameters  
 [in] `pMenuPopup`  
 A pointer to the pop-up menu.  
  
 [in] `pBar`  
 A pointer to the tear-off bar.  
  
## Return Value  
 `TRUE` to allow the pop-up menu with the tear-off bar to be made activate; otherwise `FALSE`. The default is `TRUE`.  
  
## Remarks  
 Override this function when you want to implement a special setup for the tear-off bar. The default implementation does nothing.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)