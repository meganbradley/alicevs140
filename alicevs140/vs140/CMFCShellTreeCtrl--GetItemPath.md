---
title: "CMFCShellTreeCtrl::GetItemPath"
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
ms.assetid: 037b34ba-6b01-4bbf-be41-72e181d7d1c6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellTreeCtrl::GetItemPath
Retrieves the path of an item in the [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md) object.  
  
## Syntax  
  
```  
BOOL GetItemPath(  
   CString& strPath,  
   HTREEITEM htreeItem = NULL  
) const;  
```  
  
#### Parameters  
 [out] `strPath`  
 A reference to a string parameter. The method writes the path of the item to this parameter.  
  
 [in] `htreeItem`  
 The method retrieves the path for this tree control item.  
  
## Return Value  
 Nonzero if successful; 0 otherwise.  
  
## Remarks  
 If this method fails, `strPath` contains the empty string.  
  
 If you do not specify `hTreeItem`, this method tries to obtain the string for the currently selected item. If no item is selected and `hTreeItem` is `NULL`, this method fails.  
  
## Requirements  
 **Header:** afxshelltreectrl.h  
  
## See Also  
 [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)