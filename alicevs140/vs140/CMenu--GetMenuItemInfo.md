---
title: "CMenu::GetMenuItemInfo"
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
ms.assetid: 58df6bcd-f784-4db8-9f8c-0483c633f8fe
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::GetMenuItemInfo
Retrieves information about a menu item.  
  
## Syntax  
  
```  
  
      BOOL GetMenuItemInfo(  
   UINT uItem,  
   LPMENUITEMINFO lpMenuItemInfo,  
   BOOL fByPos = FALSE   
);  
```  
  
#### Parameters  
 `uItem`  
 Identifier or position of the menu item to get information about. The meaning of this parameter depends on the value of `ByPos`.  
  
 `lpMenuItemInfo`  
 A pointer to a [MENUITEMINFO](http://msdn.microsoft.com/library/windows/desktop/ms647578), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)], that contains information about the menu.  
  
 `fByPos`  
 Value specifying the meaning of `nIDItem`. By default, `ByPos` is **FALSE**, which indicates that uItem is a menu item identifier. If `ByPos` is not set to **FALSE**, it indicates a menu item position.  
  
## Return Value  
 If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, use the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This member function implements the behavior of the of the Win32 function [GetMenuItemInfo](http://msdn.microsoft.com/library/windows/desktop/ms647980), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. Note that in the MFC implementation of `GetMenuItemInfo`, you do not use a handle to a menu.  
  
## Example  
 [!CODE [NVC_MFCWindowing#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#26)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetMenu](../vs140/CWnd--GetMenu.md)   
 [CMenu::GetMenuItemCount](../vs140/CMenu--GetMenuItemCount.md)   
 [CMenu::GetMenuItemID](../vs140/CMenu--GetMenuItemID.md)