---
title: "CShellManager::GetParentItem"
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
ms.assetid: f9d9c49b-87e6-48c8-9682-5b58082e2d75
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CShellManager::GetParentItem
Retrieves the parent of a pointer to an item identifier list (PIDL).  
  
## Syntax  
  
```  
int GetParentItem(  
   LPCITEMIDLIST lpidl,  
   LPITEMIDLIST& lpidlParent   
);  
```  
  
#### Parameters  
 [in] `lpidl`  
 A PIDL whose parent will be retrieved.  
  
 [out] `lpidlParent`  
 A reference to a PIDL where the method will store the result.  
  
## Return Value  
 The level of the parent PIDL.  
  
## Remarks  
 The level of a PIDL is relative to the desktop. The desktop PIDL is considered to have a level of 0.  
  
## Requirements  
 **Header:** afxshellmanager.h  
  
## See Also  
 [CShellManager Class](../vs140/CShellManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)