---
title: "CShellManager::CreateItem"
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
ms.assetid: 1c002463-c53b-4ffc-845d-907cf961d52e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CShellManager::CreateItem
Creates a new PIDL.  
  
## Syntax  
  
```  
LPITEMIDLIST CreateItem(  
   UINT cbSize   
);  
```  
  
#### Parameters  
 [in] `cbSize`  
 The size of the item list.  
  
## Return Value  
 A pointer to the created item list if successful; otherwise `NULL`.  
  
## Requirements  
 **Header:** afxshellmanager.h  
  
## See Also  
 [CShellManager Class](../vs140/CShellManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)