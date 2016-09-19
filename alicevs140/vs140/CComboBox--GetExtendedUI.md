---
title: "CComboBox::GetExtendedUI"
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
ms.assetid: fad4b45d-587e-445b-9e16-c536c1e22708
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetExtendedUI
Call the `GetExtendedUI` member function to determine whether a combo box has the default user interface or the extended user interface.  
  
## Syntax  
  
```  
  
BOOL GetExtendedUI( ) const;  
```  
  
## Return Value  
 Nonzero if the combo box has the extended user interface; otherwise 0.  
  
## Remarks  
 The extended user interface can be identified in the following ways:  
  
-   Clicking the static control displays the list box only for combo boxes with the [CBS_DROPDOWNLIST](../vs140/Combo-Box-Styles.md) style.  
  
-   Pressing the DOWN ARROW key displays the list box (F4 is disabled).  
  
 Scrolling in the static control is disabled when the item list is not visible (arrow keys are disabled).  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#19)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetExtendedUI](../vs140/CComboBox--SetExtendedUI.md)   
 [CB_GETEXTENDEDUI](http://msdn.microsoft.com/library/windows/desktop/bb775855)