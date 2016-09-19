---
title: "CMFCShellListCtrl::GetItemPath"
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
ms.assetid: 39b3a02b-e4f6-464b-8752-371a6d8ccb1a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellListCtrl::GetItemPath
Retrieves the path for an item.  
  
## Syntax  
  
```  
BOOL GetItemPath(  
   CString& strPath,  
   int iItem   
) const;  
```  
  
#### Parameters  
 [out] `strPath`  
 A reference to a string that receives the path.  
  
 [in] `iItem`  
 The index of the list item.  
  
## Return Value  
 `TRUE` if successful; `FALSE` otherwise.  
  
## Remarks  
 The index supplied by `iItem` is based on the items currently displayed by the [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md) object.  
  
## Requirements  
 **Header:** afxshelllistctrl.h  
  
## See Also  
 [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)