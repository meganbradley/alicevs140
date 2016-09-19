---
title: "CListCtrl::GetItemState"
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
ms.assetid: a3df96c6-5494-4dd7-aa07-ec25c4dd37dd
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetItemState
Retrieves the state of a list view item.  
  
## Syntax  
  
```  
  
      UINT GetItemState(  
   int nItem,  
   UINT nMask   
) const;  
```  
  
#### Parameters  
 `nItem`  
 The index of the item whose state is to be retrieved.  
  
 `nMask`  
 Mask specifying which of the item's state flags to return.  
  
## Return Value  
 The state flags for the specified list view item.  
  
## Remarks  
 An item's state is specified by the **state** member of the [LVITEM](http://msdn.microsoft.com/library/windows/desktop/bb774760) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. When you specify or change an item's state, the **stateMask** member specifies which state bits you want to change.  
  
## Example  
 See the example for [CListCtrl::GetTopIndex](../vs140/CListCtrl--GetTopIndex.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetItemState](../vs140/CListCtrl--SetItemState.md)   
 [CListCtrl::GetItem](../vs140/CListCtrl--GetItem.md)