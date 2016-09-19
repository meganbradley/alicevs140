---
title: "CComboBox::SetItemData"
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
ms.assetid: 61735c4e-b75f-46c9-a7a5-333460145d6a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetItemData
Sets the 32-bit value associated with the specified item in a combo box.  
  
## Syntax  
  
```  
  
      int SetItemData(  
   int nIndex,  
   DWORD_PTR dwItemData   
);  
```  
  
#### Parameters  
 `nIndex`  
 Contains a zero-based index to the item to set.  
  
 `dwItemData`  
 Contains the new value to associate with the item.  
  
## Return Value  
 **CB_ERR** if an error occurs.  
  
## Remarks  
 Use the `SetItemDataPtr` member function if the 32-bit item is to be a pointer.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#36)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetItemData](../vs140/CComboBox--GetItemData.md)   
 [CComboBox::GetItemDataPtr](../vs140/CComboBox--GetItemDataPtr.md)   
 [CComboBox::SetItemDataPtr](../vs140/CComboBox--SetItemDataPtr.md)   
 [CB_SETITEMDATA](http://msdn.microsoft.com/library/windows/desktop/bb775909)   
 [CComboBox::AddString](../vs140/CComboBox--AddString.md)   
 [CComboBox::InsertString](../vs140/CComboBox--InsertString.md)