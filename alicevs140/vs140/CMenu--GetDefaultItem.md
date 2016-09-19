---
title: "CMenu::GetDefaultItem"
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
ms.assetid: 998043e4-4110-427a-9faf-6999afdaaf07
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::GetDefaultItem
Determines the default menu item on the specified menu.  
  
## Syntax  
  
```  
  
      UINT GetDefaultItem(  
   UINT gmdiFlags,  
   BOOL fByPos = FALSE   
);  
```  
  
#### Parameters  
 *gmdiFlags*  
 Value specifying how the function searches for menu items. This parameter can be none, one, or a combination of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|**GMDI_GOINTOPOPUPS**|Specifies that, if the default item is one that opens a submenu, the function is to search in the corresponding submenu recursively. If the submenu has no default item, the return value identifies the item that opens the submenu.<br /><br /> By default, the function returns the first default item on the specified menu, regardless of whether it is an item that opens a submenu.|  
|**GMDI_USEDISABLED**|Specifies that the function is to return a default item, even if it is disabled.<br /><br /> By default, the function skips disabled or grayed items.|  
  
 `fByPos`  
 Value specifying whether to retrieve the menu item's identifier or its position. If this parameter is **FALSE**, the identifier is returned. Otherwise, the position is returned.  
  
## Return Value  
 If the function succeeds, the return value is the identifier or position of the menu item. If the function fails, the return value is - 1.  
  
## Remarks  
 This member function implements the behavior of the Win32 function [GetMenuDefaultItem](http://msdn.microsoft.com/library/windows/desktop/ms647976), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CMenu::InsertMenu](../vs140/CMenu--InsertMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::SetDefaultItem](../vs140/CMenu--SetDefaultItem.md)