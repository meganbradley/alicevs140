---
title: "CTreeCtrl::SetItemState"
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
ms.assetid: df7d7102-1c63-4f6c-a553-10e41d49982c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetItemState
Sets the state of the item specified by `hItem`.  
  
## Syntax  
  
```  
  
      BOOL SetItemState(  
   HTREEITEM hItem,  
   UINT nState,  
   UINT nStateMask   
);  
```  
  
#### Parameters  
 `hItem`  
 Handle of the item whose state is to be set.  
  
 `nState`  
 Specifies new states for the item.  
  
 `nStateMask`  
 Specifies which states are to be changed.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 For information on states, see [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md).  
  
## Example  
 See the example for [CTreeCtrl::GetItemState](../vs140/CTreeCtrl--GetItemState.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetItem](../vs140/CTreeCtrl--GetItem.md)   
 [CTreeCtrl::GetItemState](../vs140/CTreeCtrl--GetItemState.md)