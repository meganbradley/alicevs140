---
title: "CComboBox::GetCurSel"
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
ms.assetid: 9d17af2d-811c-42ce-931f-0f50ad5e9269
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetCurSel
Call this member function to determine which item in the combo box is selected.  
  
## Syntax  
  
```  
  
int GetCurSel( ) const;  
```  
  
## Return Value  
 The zero-based index of the currently selected item in the list box of a combo box, or **CB_ERR** if no item is selected.  
  
## Remarks  
 `GetCurSel` returns an index into the list.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#15)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetCurSel](../vs140/CComboBox--SetCurSel.md)   
 [CB_GETCURSEL](http://msdn.microsoft.com/library/windows/desktop/bb775845)