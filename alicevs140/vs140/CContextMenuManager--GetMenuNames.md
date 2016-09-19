---
title: "CContextMenuManager::GetMenuNames"
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
ms.assetid: e4b704f3-b901-4410-a350-736bc30c79cb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::GetMenuNames
Returns the list of menu names added to the [CContextMenuManager](../vs140/CContextMenuManager-Class.md).  
  
## Syntax  
  
```  
void GetMenuNames(  
   CStringList& listOfNames   
) const;  
```  
  
#### Parameters  
 [out] `listOfNames`  
 A reference to a [CStringList](../vs140/CStringList-Class.md) parameter. This method writes the list of menu names to this parameter.  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)