---
title: "CMenu::SetMenuInfo"
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
ms.assetid: fa6925b1-4ba5-4498-8a1d-fc1e890e17ec
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::SetMenuInfo
Sets information for a menu.  
  
## Syntax  
  
```  
  
      BOOL SetMenuInfo(   
   LPCMENUINFO lpcmi   
);  
```  
  
#### Parameters  
 `lpcmi`  
 A pointer to a [MENUINFO](http://msdn.microsoft.com/library/windows/desktop/ms647575) structure containing information for the menu.  
  
## Return Value  
 If the function succeeds, the return value is nonzero; otherwise, the return value is zero.  
  
## Remarks  
 Call this function to set specific information about the menu.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::GetMenuInfo](../vs140/CMenu--GetMenuInfo.md)