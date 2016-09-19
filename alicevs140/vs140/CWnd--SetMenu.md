---
title: "CWnd::SetMenu"
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
ms.assetid: 548b9ec2-77f2-4127-8a46-ce96c4c269c9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetMenu
Sets the current menu to the specified menu.  
  
## Syntax  
  
```  
  
      BOOL SetMenu(  
   CMenu* pMenu   
);  
```  
  
#### Parameters  
 `pMenu`  
 Identifies the new menu. If this parameter is **NULL**, the current menu is removed.  
  
## Return Value  
 Nonzero if the menu is changed; otherwise 0.  
  
## Remarks  
 Causes the window to be redrawn to reflect the menu change.  
  
 `SetMenu` will not destroy a previous menu. An application should call the [CMenu::DestroyMenu](../vs140/CMenu--DestroyMenu.md) member function to accomplish this task.  
  
## Example  
 See the example for [CMenu::LoadMenu](../vs140/CMenu--LoadMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::DestroyMenu](../vs140/CMenu--DestroyMenu.md)   
 [CMenu::LoadMenu](../vs140/CMenu--LoadMenu.md)   
 [SetMenu](http://msdn.microsoft.com/library/windows/desktop/ms647995)   
 [CWnd::GetMenu](../vs140/CWnd--GetMenu.md)