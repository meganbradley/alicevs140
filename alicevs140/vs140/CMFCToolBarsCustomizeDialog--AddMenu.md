---
title: "CMFCToolBarsCustomizeDialog::AddMenu"
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
ms.assetid: b5157fac-2c1a-451a-81cd-8864a2e061a2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::AddMenu
Loads a menu from the resources and calls [CMFCToolBarsCustomizeDialog::AddMenuCommands](../vs140/CMFCToolBarsCustomizeDialog--AddMenuCommands.md) to add that menu to the list of commands on the **Commands** page.  
  
## Syntax  
  
```  
BOOL AddMenu(  
   UINT uiMenuResId   
);  
```  
  
#### Parameters  
 [in] `uiMenuResId`  
 Specifies the resource ID of a menu to load.  
  
## Return Value  
 `TRUE` if a menu was added successfully; otherwise `FALSE`.  
  
## Remarks  
 In the call to `AddMenuCommands`, `bPopup` is `FALSE`. As a result, that method does not add menu items that contain submenus to the list of commands. This method does add the menu items in the submenus to the list of commands.  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)