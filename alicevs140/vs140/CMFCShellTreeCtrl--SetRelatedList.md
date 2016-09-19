---
title: "CMFCShellTreeCtrl::SetRelatedList"
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
ms.assetid: e1c637ec-1b13-4fd9-a814-8888554a028c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellTreeCtrl::SetRelatedList
Associates a [CMFCShellListCtrl](../vs140/CMFCShellListCtrl-Class.md) object with a [CMFCShellTreeCtrl](../vs140/CMFCShellTreeCtrl-Class.md) object.  
  
## Syntax  
  
```  
void SetRelatedList(  
   CMFCShellListCtrl* pShellList   
);  
```  
  
#### Parameters  
 [in] `pShellList`  
 A pointer to a `CMFCShellListCtrl` object.  
  
## Remarks  
 This method associates a `CMFCShellListCtrl` with a `CMFCShellTreeCtrl`. These objects may be displayed as an Explorer-like window: if the user selects an object in the `CMFCShellTreeCtrl`, the associated items in the `CMFCShellListCtrl` will be automatically updated.  
  
 Use the method [CMFCShellTreeCtrl::GetRelatedList](../vs140/CMFCShellTreeCtrl--GetRelatedList.md) to retrieve the `CMFCShellListCtrl` associated with a `CMFCShellTreeCtrl`.  
  
## Requirements  
 **Header:** afxshelltreectrl.h  
  
## See Also  
 [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCShellTreeCtrl::GetRelatedList](../vs140/CMFCShellTreeCtrl--GetRelatedList.md)   
 [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md)