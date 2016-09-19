---
title: "CVSListBox::SetItemData"
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
ms.assetid: cb5713c9-1c08-4745-bc61-774e09ee4c5a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVSListBox::SetItemData
Associates an application-specific 32-bit value with an editable list control item.  
  
## Syntax  
  
```  
virtual void SetItemData(  
   int iIndex,  
   DWORD_PTR dwData   
);  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of an editable list control item.  
  
 [in] `dwData`  
 A 32-bit value. This value can be an application-specific integer or a pointer to other data.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvslistbox.h  
  
## See Also  
 [CVSListBox Class](../vs140/CVSListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CVSListBox::GetItemData](../vs140/CVSListBox--GetItemData.md)