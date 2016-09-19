---
title: "COleIPFrameWndEx::InitUserToobars"
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
ms.assetid: c7184600-3a37-41af-a273-99169f8744ea
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::InitUserToobars
Specifies a range of control IDs that the framework assigns to the user-defined toolbars.  
  
## Syntax  
  
```  
void InitUserToolbars(  
   LPCTSTR lpszRegEntry,   
   UINT uiUserToolbarFirst,   
   UINT uiUserToolbarLast  
)  
```  
  
#### Parameters  
 [in] `lpszRegEntry`  
 The registry entry where the library stores user toolbar settings.  
  
 [in] `uiUserToolbarFirst`  
 Control ID assigned to the first user-defined toolbar.  
  
 [in] `uiUserToolbarLast`  
 Control ID assigned to the last user-defined toolbar.  
  
## Remarks  
 Use this function to initialize a range of control IDs for assignment to toolbars that users define dynamically. The parameters `uiUserToolbarFirst` and `uiUserToolbarLast` define a range of allowed toolbar control IDs. To disable the creation of user-defined toolbars, set `uiUserToolbarFirst` or `uiUserToolbarLast` to -1.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)