---
title: "CHeaderCtrl::InsertItem"
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
ms.assetid: 5b4abebd-be80-453f-a09c-89cb26d6a53d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::InsertItem
Inserts a new item into a header control at the specified index.  
  
## Syntax  
  
```  
  
      int InsertItem(  
   int nPos,  
   HDITEM* phdi   
);  
```  
  
#### Parameters  
 `nPos`  
 The zero-based index of the item to be inserted. If the value is zero, the item is inserted at the beginning of the header control. If the value is greater than the maximum value, the item is inserted at the end of the header control.  
  
 *phdi*  
 Pointer to an [HDITEM](http://msdn.microsoft.com/library/windows/desktop/bb775247) structure that contains information about the item to be inserted.  
  
## Return Value  
 Index of the new item if successful; otherwise – 1.  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#12)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::DeleteItem](../vs140/CHeaderCtrl--DeleteItem.md)   
 [CHeaderCtrl::GetItem](../vs140/CHeaderCtrl--GetItem.md)