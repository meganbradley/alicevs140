---
title: "CListCtrl::SetItemText"
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
ms.assetid: 2ee00cb9-f39a-49a1-919a-085b0fbd7f28
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetItemText
Changes the text of a list view item or subitem.  
  
## Syntax  
  
```  
  
      BOOL SetItemText(  
   int nItem,  
   int nSubItem,  
   LPCTSTR lpszText   
);  
```  
  
#### Parameters  
 `nItem`  
 Index of the item whose text is to be set.  
  
 `nSubItem`  
 Index of the subitem, or zero to set the item label.  
  
 `lpszText`  
 Pointer to a string that contains the new item text.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This method is not intended for use with controls containing the LVS_OWNERDATA window style (in fact, this will cause an assertion in Debug builds). For more information about this list control style, see [List-View Controls Overview](http://msdn.microsoft.com/library/windows/desktop/bb774735).  
  
## Example  
 See the example for [CListCtrl::InsertItem](../vs140/CListCtrl--InsertItem.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetItemText](../vs140/CListCtrl--GetItemText.md)