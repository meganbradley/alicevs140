---
title: "CComboBox::GetEditSel"
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
ms.assetid: b28d9022-129a-4025-916d-3238ac5f0216
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetEditSel
Gets the starting and ending character positions of the current selection in the edit control of a combo box.  
  
## Syntax  
  
```  
  
DWORD GetEditSel( ) const;  
```  
  
## Return Value  
 A 32-bit value that contains the starting position in the low-order word and the position of the first nonselected character after the end of the selection in the high-order word. If this function is used on a combo box without an edit control, **CB_ERR** is returned.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#18)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetEditSel](../vs140/CComboBox--SetEditSel.md)   
 [CB_GETEDITSEL](http://msdn.microsoft.com/library/windows/desktop/bb775853)