---
title: "CContextMenuManager::GetMenuByName"
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
ms.assetid: 9ff9dcc8-f712-49c5-9183-7b68cc759ae2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::GetMenuByName
Returns a handle to a specific menu.  
  
## Syntax  
  
```  
HMENU GetMenuByName(  
   LPCTSTR lpszName,  
   UINT* puiOrigResID = NULL  
) const;  
```  
  
#### Parameters  
 [in] `lpszName`  
 A string that contains the name of the menu to retrieve.  
  
 [out] `puiOrigResID`  
 A pointer to an `UINT`. This parameter contains the resource ID of the specified menu, if found.  
  
## Return Value  
 A handle to the menu that matches the name that was specified by `lpszName`. `NULL` if there is no menu called `lpszName`.  
  
## Remarks  
 If this method finds a menu that matches `lpszName`, `GetMenuByName` stores the menu resource ID in the parameter `puiOrigResID`.  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)