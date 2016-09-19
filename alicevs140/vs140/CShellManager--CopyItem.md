---
title: "CShellManager::CopyItem"
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
ms.assetid: bacc9262-868e-4b15-ac54-e92a620173e7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CShellManager::CopyItem
Copies an item list.  
  
## Syntax  
  
```  
LPITEMIDLIST CopyItem(  
   LPCITEMIDLIST pidlSource   
);  
```  
  
#### Parameters  
 [in] `pidlSource`  
 The original item list.  
  
## Return Value  
 A pointer to the newly created item list if successful; otherwise `NULL`.  
  
## Remarks  
 The newly created item list has the same size as the source item list.  
  
## Requirements  
 **Header:** afxshellmanager.h  
  
## See Also  
 [CShellManager Class](../vs140/CShellManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)