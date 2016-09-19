---
title: "CContextMenuManager::GetMenuById"
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
ms.assetid: b7f2d66d-8ac7-4c78-a212-a039f9d88f8c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::GetMenuById
Returns a handle to the menu associated with a given resource ID.  
  
## Syntax  
  
```  
HMENU GetMenuById(  
   UINT nMenuResId   
) const;  
```  
  
#### Parameters  
 [in] `nMenuResId`  
 The resource ID for the menu.  
  
## Return Value  
 A handle to the associated menu or `NULL` if the menu is not found.  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)