---
title: "CListBox::GetItemDataPtr"
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
ms.assetid: 5bfe3c55-e3c9-4dd4-81dd-647c8cc074e1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetItemDataPtr
Retrieves the application-supplied 32-bit value associated with the specified list-box item as a pointer (**void\***).  
  
## Syntax  
  
```  
  
      void* GetItemDataPtr(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item in the list box.  
  
## Return Value  
 Retrieves a pointer, or –1 if an error occurs.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#16)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::AddString](../vs140/CListBox--AddString.md)   
 [CListBox::GetItemData](../vs140/CListBox--GetItemData.md)   
 [CListBox::InsertString](../vs140/CListBox--InsertString.md)   
 [CListBox::SetItemData](../vs140/CListBox--SetItemData.md)   
 [LB_GETITEMDATA](http://msdn.microsoft.com/library/windows/desktop/bb775202)