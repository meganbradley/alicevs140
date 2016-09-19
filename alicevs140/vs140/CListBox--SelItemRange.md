---
title: "CListBox::SelItemRange"
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
ms.assetid: 50656902-20e3-45b9-87c8-e3631d732fbd
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SelItemRange
Selects multiple consecutive items in a multiple-selection list box.  
  
## Syntax  
  
```  
  
      int SelItemRange(  
   BOOL bSelect,  
   int nFirstItem,  
   int nLastItem   
);  
```  
  
#### Parameters  
 `bSelect`  
 Specifies how to set the selection. If `bSelect` is **TRUE**, the string is selected and highlighted; if **FALSE**, the highlight is removed and the string is no longer selected.  
  
 `nFirstItem`  
 Specifies the zero-based index of the first item to set.  
  
 `nLastItem`  
 Specifies the zero-based index of the last item to set.  
  
## Return Value  
 **LB_ERR** if an error occurs.  
  
## Remarks  
 Use this member function only with multiple-selection list boxes. If you need to select only one item in a multiple-selection list box — that is, if `nFirstItem` is equal to `nLastItem` — call the [SetSel](../vs140/CListBox--SetSel.md) member function instead.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#28)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_SELITEMRANGE](http://msdn.microsoft.com/library/windows/desktop/bb761329)   
 [CListBox::GetSelItems](../vs140/CListBox--GetSelItems.md)