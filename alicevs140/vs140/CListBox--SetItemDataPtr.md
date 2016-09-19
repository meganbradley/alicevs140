---
title: "CListBox::SetItemDataPtr"
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
ms.assetid: 88ede889-cf18-4058-9ba8-0011a8a7a6f0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetItemDataPtr
Sets the 32-bit value associated with the specified item in a list box to be the specified pointer (**void\***).  
  
## Syntax  
  
```  
  
      int SetItemDataPtr(  
   int nIndex,  
   void* pData   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item.  
  
 `pData`  
 Specifies the pointer to be associated with the item.  
  
## Return Value  
 **LB_ERR** if an error occurs.  
  
## Remarks  
 This pointer remains valid for the life of the list box, even though the item's relative position within the list box might change as items are added or removed. Hence, the item's index within the box can change, but the pointer remains reliable.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#35)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetItemData](../vs140/CListBox--SetItemData.md)   
 [CListBox::GetItemData](../vs140/CListBox--GetItemData.md)   
 [CListBox::GetItemDataPtr](../vs140/CListBox--GetItemDataPtr.md)   
 [LB_SETITEMDATA](http://msdn.microsoft.com/library/windows/desktop/bb761346)