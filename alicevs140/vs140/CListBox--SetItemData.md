---
title: "CListBox::SetItemData"
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
ms.assetid: 10ca5434-ebb6-4c1c-9371-6f4ef07671ff
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetItemData
Sets a 32-bit value associated with the specified item in a list box.  
  
## Syntax  
  
```  
  
      int SetItemData(  
   int nIndex,  
   DWORD_PTR dwItemData   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item.  
  
 `dwItemData`  
 Specifies the value to be associated with the item.  
  
## Return Value  
 **LB_ERR** if an error occurs.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#34)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetItemDataPtr](../vs140/CListBox--SetItemDataPtr.md)   
 [CListBox::GetItemData](../vs140/CListBox--GetItemData.md)   
 [LB_SETITEMDATA](http://msdn.microsoft.com/library/windows/desktop/bb761346)