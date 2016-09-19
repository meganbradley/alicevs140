---
title: "CMFCShellTreeCtrl::GetRelatedList"
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
ms.assetid: 66ea2905-4249-461a-aad9-73f1ac141731
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellTreeCtrl::GetRelatedList
Returns a pointer to the [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md) object that is associated with this [CMFCShellTreeCtrl](../vs140/CMFCShellTreeCtrl-Class.md) object.  
  
## Syntax  
  
```  
CMFCShellListCtrl* GetRelatedList() const;  
```  
  
## Return Value  
 A pointer to the `CMFCShellListCtrl` object that is associated with this tree control object.  
  
## Remarks  
 By using a `CMFCShellListCtrl` object together with a `CMFCShellTreeCtrl` object, you can create an Explorer-like window. Use the method [CMFCShellTreeCtrl::SetRelatedList](../vs140/CMFCShellTreeCtrl--SetRelatedList.md) to associate the two classes. After they are associated, the framework automatically updates the `CMFCShellListCtrl` if the selection in the `CMFCShellTreeCtrl` changes.  
  
## Requirements  
 **Header:** afxshelltreectrl.h  
  
## See Also  
 [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCShellTreeCtrl::SetRelatedList](../vs140/CMFCShellTreeCtrl--SetRelatedList.md)   
 [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md)