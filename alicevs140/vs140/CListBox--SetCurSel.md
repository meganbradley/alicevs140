---
title: "CListBox::SetCurSel"
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
ms.assetid: 1f354770-3acb-47e2-acf6-5ea5ddfb8822
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetCurSel
Selects a string and scrolls it into view, if necessary.  
  
## Syntax  
  
```  
  
      int SetCurSel(  
   int nSelect   
);  
```  
  
#### Parameters  
 `nSelect`  
 Specifies the zero-based index of the string to be selected. If `nSelect` is –1, the list box is set to have no selection.  
  
## Return Value  
 `LB_ERR` if an error occurs.  
  
## Remarks  
 When the new string is selected, the list box removes the highlight from the previously selected string.  
  
 Use this member function only with single-selection list boxes.  
  
 To set or remove a selection in a multiple-selection list box, use [CListBox::SetSel](../vs140/CListBox--SetSel.md).  
  
## Example  
 [!CODE [NVC_MFC_CListBox#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#32)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_SETCURSEL](http://msdn.microsoft.com/library/windows/desktop/bb761342)   
 [CListBox::GetCurSel](../vs140/CListBox--GetCurSel.md)   
 [CListBox::SetSel](../vs140/CListBox--SetSel.md)