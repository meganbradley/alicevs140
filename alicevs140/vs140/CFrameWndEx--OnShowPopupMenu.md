---
title: "CFrameWndEx::OnShowPopupMenu"
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
ms.assetid: f6d3ef56-7dd7-49cc-b3f2-f8e4776d9b2e
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnShowPopupMenu
Called by the framework when it displays a pop-up menu.  
  
## Syntax  
  
```  
virtual BOOL OnShowPopupMenu(  
   CMFCPopupMenu* pMenu  
);  
```  
  
#### Parameters  
 [in] `pMenu`  
 A pointer to a pop-up menu.  
  
## Return Value  
 `TRUE` if the pop-up menu is visible; otherwise `FALSE`.  
  
## Remarks  
 Override this method in a derived class to execute custom code when the framework displays a pop-up menu. For example, override this method to change the background color of the commands in a pop-up menu.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)