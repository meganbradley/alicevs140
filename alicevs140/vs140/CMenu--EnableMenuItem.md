---
title: "CMenu::EnableMenuItem"
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
ms.assetid: e276ba57-98c5-4606-a0a4-9e8adfafafa2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::EnableMenuItem
Enables, disables, or dims a menu item.  
  
## Syntax  
  
```  
  
      UINT EnableMenuItem(  
   UINT nIDEnableItem,  
   UINT nEnable   
);  
```  
  
#### Parameters  
 *nIDEnableItem*  
 Specifies the menu item to be enabled, as determined by `nEnable`. This parameter can specify pop-up menu items as well as standard menu items.  
  
 `nEnable`  
 Specifies the action to take. It can be a combination of **MF_DISABLED**, `MF_ENABLED`, or **MF_GRAYED**, with **MF_BYCOMMAND** or **MF_BYPOSITION**. These values can be combined by using the bitwise OR operator. These values have the following meanings:  
  
-   **MF_BYCOMMAND** Specifies that the parameter gives the command ID of the existing menu item. This is the default.  
  
-   **MF_BYPOSITION** Specifies that the parameter gives the position of the existing menu item. The first item is at position 0.  
  
-   **MF_DISABLED** Disables the menu item so that it cannot be selected but does not dim it.  
  
-   `MF_ENABLED` Enables the menu item so that it can be selected and restores it from its dimmed state.  
  
-   **MF_GRAYED** Disables the menu item so that it cannot be selected and dims it.  
  
## Return Value  
 Previous state (**MF_DISABLED**, `MF_ENABLED`, or **MF_GRAYED**) or –1 if not valid.  
  
## Remarks  
 The [CreateMenu](../vs140/CMenu--CreateMenu.md), [InsertMenu](../vs140/CMenu--InsertMenu.md), [ModifyMenu](../vs140/CMenu--ModifyMenu.md), and [LoadMenuIndirect](../vs140/CMenu--LoadMenuIndirect.md) member functions can also set the state (enabled, disabled, or dimmed) of a menu item.  
  
 Using the **MF_BYPOSITION** value requires an application to use the correct `CMenu`. If the `CMenu` of the menu bar is used, a top-level menu item (an item in the menu bar) is affected. To set the state of an item in a pop-up or nested pop-up menu by position, an application must specify the `CMenu` of the pop-up menu.  
  
 When an application specifies the **MF_BYCOMMAND** flag, Windows checks all pop-up menu items that are subordinate to the `CMenu`; therefore, unless duplicate menu items are present, using the `CMenu` of the menu bar is sufficient.  
  
## Example  
 [!CODE [NVC_MFCWindowing#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#25)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::GetMenuState](../vs140/CMenu--GetMenuState.md)   
 [EnableMenuItem](http://msdn.microsoft.com/library/windows/desktop/ms647636)