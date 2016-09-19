---
title: "CMenu::SetDefaultItem"
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
ms.assetid: db995d2e-eaaa-48e1-b4eb-e67ff5071082
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::SetDefaultItem
Sets the default menu item for the specified menu.  
  
## Syntax  
  
```  
  
      BOOL SetDefaultItem(  
   UINT uItem,  
   BOOL fByPos = FALSE   
);  
```  
  
#### Parameters  
 `uItem`  
 Identifier or position of the new default menu item or - 1 for no default item. The meaning of this parameter depends on the value of `fByPos`.  
  
 `fByPos`  
 Value specifying the meaning of `uItem`. If this parameter is **FALSE**, `uItem` is a menu item identifier. Otherwise, it is a menu item position.  
  
## Return Value  
 If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, use the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This member function implements the behavior of the Win32 function [SetMenuDefaultItem](http://msdn.microsoft.com/library/windows/desktop/ms647996), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CMenu::InsertMenu](../vs140/CMenu--InsertMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::GetDefaultItem](../vs140/CMenu--GetDefaultItem.md)