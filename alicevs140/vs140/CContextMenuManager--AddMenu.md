---
title: "CContextMenuManager::AddMenu"
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
ms.assetid: 0b6f39ba-76c2-4bb0-b60a-ebf6ee6c3deb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::AddMenu
Adds a new shortcut menu to the [CContextMenuManager](../vs140/CContextMenuManager-Class.md).  
  
## Syntax  
  
```  
BOOL AddMenu(  
   UINT uiMenuNameResId,  
   UINT uiMenuResId   
);  
  
BOOL AddMenu(  
   LPCTSTR lpszName,  
   UINT uiMenuResId   
);  
```  
  
#### Parameters  
 [in] `uiMenuNameResId`  
 A resource ID for a string that contains the name for the new menu.  
  
 [in] `uiMenuResId`  
 The menu resource ID.  
  
 [in] `lpszName`  
 A string that contains the name for the new menu.  
  
## Return Value  
 Nonzero if the method was successful; 0 if the method fails.  
  
## Remarks  
 This method fails if `uiMenuResId` is invalid or if another menu with the same name already is in the `CContextMenuManager`.  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)