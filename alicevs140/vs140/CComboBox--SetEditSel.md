---
title: "CComboBox::SetEditSel"
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
ms.assetid: 808d298f-82ad-40ad-8133-d55bf0638c1b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetEditSel
Selects characters in the edit control of a combo box.  
  
## Syntax  
  
```  
  
      BOOL SetEditSel(  
   int nStartChar,  
   int nEndChar   
);  
```  
  
#### Parameters  
 `nStartChar`  
 Specifies the starting position. If the starting position is set to –1, then any existing selection is removed.  
  
 `nEndChar`  
 Specifies the ending position. If the ending position is set to –1, then all text from the starting position to the last character in the edit control is selected.  
  
## Return Value  
 Nonzero if the member function is successful; otherwise 0. It is **CB_ERR** if `CComboBox` has the [CBS_DROPDOWNLIST](../vs140/Combo-Box-Styles.md) style or does not have a list box.  
  
## Remarks  
 The positions are zero-based. To select the first character of the edit control, you specify a starting position of 0. The ending position is for the character just after the last character to select. For example, to select the first four characters of the edit control, you would use a starting position of 0 and an ending position of 4.  
  
> [!NOTE]
>  This function is not supported by the Windows **ComboBoxEx** control. For more information on this control, see [ComboBoxEx Controls](http://msdn.microsoft.com/library/windows/desktop/bb775738) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CComboBox::GetEditSel](../vs140/CComboBox--GetEditSel.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetEditSel](../vs140/CComboBox--GetEditSel.md)   
 [CB_SETEDITSEL](http://msdn.microsoft.com/library/windows/desktop/bb775903)