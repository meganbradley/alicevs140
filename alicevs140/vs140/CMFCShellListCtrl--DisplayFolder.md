---
title: "CMFCShellListCtrl::DisplayFolder"
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
ms.assetid: 249fa1c3-594d-4174-b4b7-bc0de6a4fb7b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCShellListCtrl::DisplayFolder
Displays a list of items that are contained in the provided folder.  
  
## Syntax  
  
```  
virtual HRESULT DisplayFolder(  
   LPCTSTR lpszPath   
);  
virtual HRESULT DisplayFolder(  
   LPAFX_SHELLITEMINFO lpItemInfo   
);  
```  
  
#### Parameters  
 [in] `lpszPath`  
 A string that contains the path of a folder.  
  
 [in] `lpItemInfo`  
 A pointer to a `LPAFX_SHELLITEMINFO` structure that describes a folder to display.  
  
## Return Value  
 `S_OK` if successful; `E_FAIL` otherwise.  
  
## Requirements  
 **Header:** afxshelllistctrl.h  
  
## See Also  
 [CMFCShellListCtrl Class](../vs140/CMFCShellListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)