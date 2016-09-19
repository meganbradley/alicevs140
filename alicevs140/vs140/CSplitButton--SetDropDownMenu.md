---
title: "CSplitButton::SetDropDownMenu"
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
ms.assetid: 02d2bdc7-7dbc-4470-a4ed-3a00022e0232
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitButton::SetDropDownMenu
Sets the drop-down menu that is displayed when a user clicks the drop-down arrow of the current split button control.  
  
## Syntax  
  
```  
void SetDropDownMenu(  
    UINT nMenuId,   
    UINT nSubMenuId  
);  
void SetDropDownMenu(  
    CMenu* pMenu  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nMenuId`|The resource ID of the menu bar.|  
|[in] `nSubMenuId`|The resource ID of a submenu.|  
|[in] `pMenu`|Pointer to a [CMenu](../vs140/CMenu-Class.md) object that specifies a submenu. The `CSplitButton` object deletes the `CMenu` object and its associated `HMENU` when the `CSplitButton` object goes out of scope.|  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Remarks  
 The `nMenuId` parameter identifies a menu bar, which is a horizontal list of menu bar items. The `nSubMenuId` parameter is a zero-based index number that identifies a submenu, which is the drop-down list of menu items associated with each menu bar item. For example, a typical application has a menu that contains the menu bar items, "File," "Edit," and "Help." The "File" menu bar item has a submenu that contains the menu items, "Open," "Close" and "Exit." When the drop-down arrow of the split-button control is clicked, the control displays the specified submenu, not the menu bar.  
  
 The following figure depicts a dialog box that contains a pager control and a (1) split button control. The (2) drop-down arrow has already been clicked and the (3) submenu is displayed.  
  
 ![Dialog with a splitbutton and pager control.](../vs140/media/SplitButton_Pager.png "SplitButton_Pager")  
  
## Example  
 The first statement in the following code example demonstrates the [CSplitButton::SetDropDownMenu](../vs140/CSplitButton--SetDropDownMenu.md) method. We created the menu with the Visual Studio resource editor, which automatically named the menu bar ID, `IDR_MENU1`. The `nSubMenuId` parameter, which is zero, refers to the only submenu of the menu bar.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#1)]  
  
## See Also  
 [CSplitButton Class](../vs140/CSplitButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)