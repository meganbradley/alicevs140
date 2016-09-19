---
title: "CComboBox::SetCurSel"
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
ms.assetid: caa9677b-aefe-4c97-8ef1-97a468737870
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetCurSel
Selects a string in the list box of a combo box.  
  
## Syntax  
  
```  
  
      int SetCurSel(  
   int nSelect   
);  
```  
  
#### Parameters  
 `nSelect`  
 Specifies the zero-based index of the string to select. If –1, any current selection in the list box is removed and the edit control is cleared.  
  
## Return Value  
 The zero-based index of the item selected if the message is successful. The return value is **CB_ERR** if `nSelect` is greater than the number of items in the list or if `nSelect` is set to –1, which clears the selection.  
  
## Remarks  
 If necessary, the list box scrolls the string into view (if the list box is visible). The text in the edit control of the combo box is changed to reflect the new selection. Any previous selection in the list box is removed.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#33)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetCurSel](../vs140/CComboBox--GetCurSel.md)   
 [CB_SETCURSEL](http://msdn.microsoft.com/library/windows/desktop/bb775899)