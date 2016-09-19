---
title: "CComboBox::ShowDropDown"
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
ms.assetid: a8dec9b8-d827-4ad7-a4f3-889420fd1a8f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::ShowDropDown
Shows or hides the list box of a combo box that has the [CBS_DROPDOWN](../vs140/Combo-Box-Styles.md) or [CBS_DROPDOWNLIST](../vs140/Combo-Box-Styles.md) style.  
  
## Syntax  
  
```  
  
      void ShowDropDown(  
   BOOL bShowIt = TRUE   
);  
```  
  
#### Parameters  
 *bShowIt*  
 Specifies whether the drop-down list box is to be shown or hidden. A value of **TRUE** shows the list box. A value of **FALSE** hides the list box.  
  
## Remarks  
 By default, a combo box of this style will show the list box.  
  
 This member function has no effect on a combo box created with the [CBS_SIMPLE](../vs140/Combo-Box-Styles.md) style.  
  
## Example  
 See the example for [CComboBox::GetDroppedState](../vs140/CComboBox--GetDroppedState.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CB_SHOWDROPDOWN](http://msdn.microsoft.com/library/windows/desktop/bb775919)