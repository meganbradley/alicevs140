---
title: "CListCtrl::GetItem"
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
ms.assetid: f4617c9a-be1f-4288-aeee-19f4d0e210fc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetItem
Retrieves some or all of a list view item's attributes.  
  
## Syntax  
  
```  
  
      BOOL GetItem(  
   LVITEM* pItem   
) const;  
```  
  
#### Parameters  
 `pItem`  
 Pointer to an [LVITEM](http://msdn.microsoft.com/library/windows/desktop/bb774760) structure that receives the item's attributes.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The **LVITEM** structure specifies or receives the attributes of a list view item.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetItem](../vs140/CListCtrl--SetItem.md)