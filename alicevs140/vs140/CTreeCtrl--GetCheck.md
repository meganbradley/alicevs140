---
title: "CTreeCtrl::GetCheck"
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
ms.assetid: c32c3ff1-6b75-46f7-bdd5-3b4431a36601
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetCheck
Call this member function to retrieve an item's check state.  
  
## Syntax  
  
```  
  
      BOOL GetCheck(  
   HTREEITEM hItem   
) const;  
```  
  
#### Parameters  
 `hItem`  
 The **HTREEITEM** about which to receive the state information.  
  
## Return Value  
 Nonzero if the tree control item is checked; otherwise 0.  
  
## Example  
 See the example for [CTreeCtrl::SetCheck](../vs140/CTreeCtrl--SetCheck.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetCheck](../vs140/CTreeCtrl--SetCheck.md)