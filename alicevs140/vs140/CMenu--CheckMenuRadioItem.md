---
title: "CMenu::CheckMenuRadioItem"
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
ms.assetid: 981157c5-c404-4214-a37f-dc40789dec93
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::CheckMenuRadioItem
Checks a specified menu item and makes it a radio item.  
  
## Syntax  
  
```  
  
      BOOL CheckMenuRadioItem(  
   UINT nIDFirst,  
   UINT nIDLast,  
   UINT nIDItem,  
   UINT nFlags   
);  
```  
  
#### Parameters  
 `nIDFirst`  
 Specifies (as an ID or offset, depending on the value of `nFlags`) the first menu item in the radio button group.  
  
 `nIDLast`  
 Specifies (as an ID or offset, depending on the value of `nFlags`) the last menu item in the radio button group.  
  
 `nIDItem`  
 Specifies (as an ID or offset, depending on the value of `nFlags`) the item in the group which will be checked with a radio button.  
  
 `nFlags`  
 Specifies interpretation of `nIDFirst`, `nIDLast`, and `nIDItem` in the following way:  
  
|nFlags|Interpretation|  
|------------|--------------------|  
|**MF_BYCOMMAND**|Specifies that the parameter gives the command ID of the existing menu item. This is the default if neither **MF_BYCOMMAND** nor **MF_BYPOSITION** is set.|  
|**MF_BYPOSITION**|Specifies that the parameter gives the position of the existing menu item. The first item is at position 0.|  
  
## Return Value  
 Nonzero if successful; otherwise 0  
  
## Remarks  
 At the same time, the function unchecks all other menu items in the associated group and clears the radio-item type flag for those items. The checked item is displayed using a radio button (or bullet) bitmap instead of a check mark bitmap.  
  
## Example  
 See the example for [ON_COMMAND_RANGE](../vs140/ON_COMMAND_RANGE.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::CheckMenuItem](../vs140/CMenu--CheckMenuItem.md)   
 [CMenu::GetMenuState](../vs140/CMenu--GetMenuState.md)   
 [CheckMenuRadioItem](http://msdn.microsoft.com/library/windows/desktop/ms647621)