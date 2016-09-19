---
title: "CListBox::GetItemData"
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
ms.assetid: eeb2b4f3-f5f0-466b-8312-200592f17c9f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetItemData
Retrieves the application-supplied doubleword value associated with the specified list-box item.  
  
## Syntax  
  
```  
  
      DWORD_PTR GetItemData(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item in the list box.  
  
## Return Value  
 The 32-bit value associated with the item, or **LB_ERR** if an error occurs.  
  
## Remarks  
 The doubleword value was the `dwItemData` parameter of a [SetItemData](../vs140/CListBox--SetItemData.md) call.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#15)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::AddString](../vs140/CListBox--AddString.md)   
 [CListBox::GetItemDataPtr](../vs140/CListBox--GetItemDataPtr.md)   
 [CListBox::SetItemDataPtr](../vs140/CListBox--SetItemDataPtr.md)   
 [CListBox::InsertString](../vs140/CListBox--InsertString.md)   
 [CListBox::SetItemData](../vs140/CListBox--SetItemData.md)   
 [LB_GETITEMDATA](http://msdn.microsoft.com/library/windows/desktop/bb775202)