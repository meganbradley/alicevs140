---
title: "CVSListBox::GetItemData"
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
ms.assetid: 645bc84e-4e5e-4273-b4f4-ea138e8a9343
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVSListBox::GetItemData
Retrieves an application-specific 32-bit value that is associated with an editable list control item.  
  
## Syntax  
  
```  
virtual DWORD_PTR GetItemData(  
   int iIndex   
) const;  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of an editable list control item.  
  
## Return Value  
 The 32-bit value that is associated with the specified item.  
  
## Remarks  
 Use the [CVSListBox::SetItemData](../vs140/CVSListBox--SetItemData.md) or [CVSListBox::AddItem](../vs140/CVSListBox--AddItem.md) method to associate the 32-bit value with the list control item. This value can be an application-specific integer or a pointer to other data.  
  
## Requirements  
 **Header:** afxvslistbox.h  
  
## See Also  
 [CVSListBox Class](../vs140/CVSListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)