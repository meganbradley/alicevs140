---
title: "CListBox::DeleteString"
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
ms.assetid: 905c25c0-3e44-4d98-b77f-cfbc5fa067a4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::DeleteString
Deletes the item in position `nIndex` from the list box.  
  
## Syntax  
  
```  
  
      int DeleteString(  
   UINT nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the string to be deleted.  
  
## Return Value  
 A count of the strings remaining in the list. The return value is **LB_ERR** if `nIndex` specifies an index greater than the number of items in the list.  
  
## Remarks  
 All items following `nIndex` now move down one position. For example, if a list box contains two items, deleting the first item will cause the remaining item to now be in the first position. `nIndex`=0 for the item in the first position.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#7)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_DELETESTRING](http://msdn.microsoft.com/library/windows/desktop/bb775183)   
 [CListBox::AddString](../vs140/CListBox--AddString.md)   
 [CListBox::InsertString](../vs140/CListBox--InsertString.md)