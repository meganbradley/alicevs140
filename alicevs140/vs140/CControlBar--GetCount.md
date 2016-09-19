---
title: "CControlBar::GetCount"
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
ms.assetid: fe108afb-19a8-497b-9bbe-cfabff454830
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::GetCount
Returns the number of non-`HWND` items on the `CControlBar` object.  
  
## Syntax  
  
```  
  
int GetCount( ) const;  
```  
  
## Return Value  
 The number of non-`HWND` items on the `CControlBar` object. This function returns 0 for a [CDialogBar](../vs140/CDialogBar-Class.md) object.  
  
## Remarks  
 The type of the item depends on the derived object: panes for [CStatusBar](../vs140/CStatusBar-Class.md) objects, and buttons and separators for [CToolBar](../vs140/CToolBar-Class.md) objects.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::SetButtons](../vs140/CToolBar--SetButtons.md)   
 [CStatusBar::SetIndicators](../vs140/CStatusBar--SetIndicators.md)   
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [CDialogBar Class](../vs140/CDialogBar-Class.md)