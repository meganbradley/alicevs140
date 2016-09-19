---
title: "CListBox::GetSel"
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
ms.assetid: 26551d2a-ed03-4541-8ba2-bf3d28b4e8de
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetSel
Retrieves the selection state of an item.  
  
## Syntax  
  
```  
  
      int GetSel(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item.  
  
## Return Value  
 A positive number if the specified item is selected; otherwise, it is 0. The return value is `LB_ERR` if an error occurs.  
  
## Remarks  
 This member function works with both single- and multiple-selection list boxes.  
  
 To retrieve the index of the currently-selected list box item, use [CListBox::GetCurSel](../vs140/CListBox--GetCurSel.md).  
  
## Example  
 [!CODE [NVC_MFC_CListBox#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#19)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_GETSEL](http://msdn.microsoft.com/library/windows/desktop/bb775212)   
 [CListBox::SetSel](../vs140/CListBox--SetSel.md)   
 [CListBox::GetCurSel](../vs140/CListBox--GetCurSel.md)