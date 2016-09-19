---
title: "CListCtrl::Update"
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
ms.assetid: c1334675-fe35-4c0c-8840-9aa3b6e53f08
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::Update
Forces the list view control to repaint the item specified by `nItem`.  
  
## Syntax  
  
```  
  
      BOOL Update(  
   int nItem   
);  
```  
  
#### Parameters  
 `nItem`  
 Index of the item to be updated.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This function also arranges the list view control if it has the `LVS_AUTOARRANGE` style.  
  
## Example  
 See the example for [CListCtrl::GetSelectedCount](../vs140/CListCtrl--GetSelectedCount.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::DrawItem](../vs140/CListCtrl--DrawItem.md)