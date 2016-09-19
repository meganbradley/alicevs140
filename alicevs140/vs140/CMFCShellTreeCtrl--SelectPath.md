---
title: "CMFCShellTreeCtrl::SelectPath"
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
ms.assetid: 28a7e0c6-da46-402f-8185-0444b5e3e177
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellTreeCtrl::SelectPath
Selects an item in the [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md) based on the supplied path.  
  
## Syntax  
  
```  
BOOL SelectPath(  
   LPCTSTR lpszPath   
);  
BOOL SelectPath(  
   LPCITEMIDLIST lpidl   
);  
```  
  
#### Parameters  
 [in] `lpszPath`  
 A string that specifies the path of an item.  
  
 [in] `lpidl`  
 A PIDL that specifies the item  
  
## Return Value  
 `S_OK` if successful; `E_FAIL` otherwise.  
  
## Requirements  
 **Header:** afxshelltreectrl.h  
  
## See Also  
 [CMFCShellTreeCtrl Class](../vs140/CMFCShellTreeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)