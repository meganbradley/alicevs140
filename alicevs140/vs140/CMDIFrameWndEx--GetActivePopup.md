---
title: "CMDIFrameWndEx::GetActivePopup"
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
ms.assetid: 5fe524c4-9e22-4818-8a41-5b1319fcbd98
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::GetActivePopup
Returns a pointer to the currently displayed popup menu.  
  
## Syntax  
  
```  
CMFCPopupMenu* GetActivePopup() const;  
```  
  
## Return Value  
 A pointer to the active popup menu; `NULL` if no popup menu is active.  
  
## Remarks  
 Use this function to obtain a pointer to the [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) object that is currently displayed.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)