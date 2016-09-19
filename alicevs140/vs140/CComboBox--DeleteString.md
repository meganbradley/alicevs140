---
title: "CComboBox::DeleteString"
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
ms.assetid: b49c4ef5-7d1a-4968-a841-47a3ac42db08
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::DeleteString
Deletes the item in position `nIndex` from the combo box.  
  
## Syntax  
  
```  
  
      int DeleteString(  
   UINT nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the index to the string that is to be deleted.  
  
## Return Value  
 If the return value is greater than or equal to 0, then it is a count of the strings remaining in the list. The return value is **CB_ERR** if `nIndex` specifies an index greater than the number of items in the list.  
  
## Remarks  
 All items following `nIndex` now move down one position. For example, if a combo box contains two items, deleting the first item will cause the remaining item to now be in the first position. `nIndex`=0 for the item in the first position.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#9)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::InsertString](../vs140/CComboBox--InsertString.md)   
 [CComboBox::AddString](../vs140/CComboBox--AddString.md)   
 [CB_DELETESTRING](http://msdn.microsoft.com/library/windows/desktop/bb775830)