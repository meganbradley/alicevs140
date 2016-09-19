---
title: "CListBox::SetSel"
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
ms.assetid: 34ff890c-f960-4173-8147-fea0da225fb4
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetSel
Selects a string in a multiple-selection list box.  
  
## Syntax  
  
```  
  
      int SetSel(  
   int nIndex,  
   BOOL bSelect = TRUE   
);  
```  
  
#### Parameters  
 `nIndex`  
 Contains the zero-based index of the string to be set. If –1, the selection is added to or removed from all strings, depending on the value of `bSelect`.  
  
 `bSelect`  
 Specifies how to set the selection. If `bSelect` is `TRUE`, the string is selected and highlighted; if `FALSE`, the highlight is removed and the string is no longer selected. The specified string is selected and highlighted by default.  
  
## Return Value  
 `LB_ERR` if an error occurs.  
  
## Remarks  
 Use this member function only with multiple-selection list boxes.  
  
 To select an item from a single-selection list box, use [CListBox::SetCurSel](../vs140/CListBox--SetCurSel.md).  
  
## Example  
 [!CODE [NVC_MFC_CListBox#38](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#38)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetSel](../vs140/CListBox--GetSel.md)   
 [LB_SETSEL](http://msdn.microsoft.com/library/windows/desktop/bb761352)   
 [CListBox::SetCurSel](../vs140/CListBox--SetCurSel.md)