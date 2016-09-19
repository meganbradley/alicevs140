---
title: "MEASUREITEMSTRUCT Structure"
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
ms.topic: article
ms.assetid: d141ace4-47cb-46b5-a81c-ad2c5e5a8501
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MEASUREITEMSTRUCT Structure
The `MEASUREITEMSTRUCT` structure informs Windows of the dimensions of an owner-drawn control or menu item.  
  
## Syntax  
  
```  
  
      typedef struct tagMEASUREITEMSTRUCT {  
   UINT CtlType;  
   UINT CtlID;  
   UINT itemID;  
   UINT itemWidth;  
   UINT itemHeight;  
   DWORD itemData  
} MEASUREITEMSTRUCT;  
```  
  
#### Parameters  
 `CtlType`  
 Contains the control type. The values for control types are as follows:  
  
-   **ODT_COMBOBOX** Owner-draw combo box  
  
-   **ODT_LISTBOX** Owner-draw list box  
  
-   **ODT_MENU** Owner-draw menu  
  
 `CtlID`  
 Contains the control ID for a combo box, list box, or button. This member is not used for a menu.  
  
 `itemID`  
 Contains the menu-item ID for a menu or the list-box-item ID for a variable-height combo box or list box. This member is not used for a fixed-height combo box or list box, or for a button.  
  
 *itemWidth*  
 Specifies the width of a menu item. The owner of the owner-draw menu item must fill this member before it returns from the message.  
  
 *itemHeight*  
 Specifies the height of an individual item in a list box or a menu. Before it returns from the message, the owner of the owner-draw combo box, list box, or menu item must fill out this member. The maximum height of a list box item is 255.  
  
 `itemData`  
 For a combo box or list box, this member contains the value that was passed to the list box by one of the following:  
  
-   [CComboBox::AddString](../vs140/CComboBox--AddString.md)  
  
-   [CComboBox::InsertString](../vs140/CComboBox--InsertString.md)  
  
-   [CListBox::AddString](../vs140/CListBox--AddString.md)  
  
-   [CListBox::InsertString](../vs140/CListBox--InsertString.md)  
  
 For a menu, this member contains the value that was passed to the menu by one of the following:  
  
-   [CMenu::AppendMenu](../vs140/CMenu--AppendMenu.md)  
  
-   [CMenu::InsertMenu](../vs140/CMenu--InsertMenu.md)  
  
-   [CMenu::ModifyMenu](../vs140/CMenu--ModifyMenu.md)  
  
 This allows Windows to process user interaction with the control correctly. Failure to fill out the proper members in the `MEASUREITEMSTRUCT` structure will cause improper operation of the control.  
  
## Requirements  
 **Header:** winuser.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CWnd::OnMeasureItem](../vs140/CWnd--OnMeasureItem.md)