---
title: "CMenu::GetMenuInfo"
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
ms.assetid: bfbc85e8-0f01-42c7-82af-b1c4291c7dc5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::GetMenuInfo
Retrieves information for a menu.  
  
## Syntax  
  
```  
  
      BOOL GetMenuInfo(   
   LPMENUINFO lpcmi   
) const;  
```  
  
#### Parameters  
 `lpcmi`  
 A pointer to a [MENUINFO](http://msdn.microsoft.com/library/windows/desktop/ms647575) structure containing information for the menu.  
  
## Return Value  
 If the function succeeds, the return value is nonzero; otherwise, the return value is zero.  
  
## Remarks  
 Call this function to retrieve information about the menu.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::SetMenuInfo](../vs140/CMenu--SetMenuInfo.md)