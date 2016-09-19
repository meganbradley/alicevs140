---
title: "CComboBox::SetExtendedUI"
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
ms.assetid: 179c6f84-dc99-4949-8b13-24388d51924a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetExtendedUI
Call the `SetExtendedUI` member function to select either the default user interface or the extended user interface for a combo box that has the [CBS_DROPDOWN](../vs140/Combo-Box-Styles.md) or [CBS_DROPDOWNLIST](../vs140/Combo-Box-Styles.md) style.  
  
## Syntax  
  
```  
  
      int SetExtendedUI(  
   BOOL bExtended = TRUE   
);  
```  
  
#### Parameters  
 *bExtended*  
 Specifies whether the combo box should use the extended user interface or the default user interface. A value of **TRUE** selects the extended user interface; a value of **FALSE** selects the standard user interface.  
  
## Return Value  
 **CB_OKAY** if the operation is successful, or **CB_ERR** if an error occurs.  
  
## Remarks  
 The extended user interface can be identified in the following ways:  
  
-   Clicking the static control displays the list box only for combo boxes with the **CBS_DROPDOWNLIST** style.  
  
-   Pressing the DOWN ARROW key displays the list box (F4 is disabled).  
  
 Scrolling in the static control is disabled when the item list is not visible (the arrow keys are disabled).  
  
## Example  
 See the example for [CComboBox::GetExtendedUI](../vs140/CComboBox--GetExtendedUI.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetExtendedUI](../vs140/CComboBox--GetExtendedUI.md)   
 [CB_SETEXTENDEDUI](http://msdn.microsoft.com/library/windows/desktop/bb775905)