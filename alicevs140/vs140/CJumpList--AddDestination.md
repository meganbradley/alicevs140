---
title: "CJumpList::AddDestination"
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
ms.assetid: d1aea402-6951-4550-a732-25b7cac5a698
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CJumpList::AddDestination
Adds destination to the list.  
  
## Syntax  
  
```  
BOOL AddDestination(  
   LPCTSTR lpcszCategoryName,  
   LPCTSTR strDestinationPath  
);  
BOOL AddDestination(  
   LPCTSTR strCategoryName,  
   IShellItem* pShellItem  
);  
BOOL AddDestination(  
   LPCTSTR strCategoryName,  
   IShellLink* pShellLink  
);  
```  
  
#### Parameters  
 `lpcszCategoryName`  
 Specifies a category name. If the specified category does not exist, it will be created.  
  
 `strDestinationPath`  
 Specifies a path to destination file.  
  
 `strCategoryName`  
 Specifies a category name. If the specified category does not exist, it will be created.  
  
 `pShellItem`  
 Specifies a Shell Item representing the destination being added.  
  
 `pShellLink`  
 Specifies a Shell Link representing the destination being added.  
  
## Return Value  
  
## Remarks  
 The instance of `CJumpList` internally accumulates added destinations and then commits them in `CommitList`.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CJumpList](../vs140/CJumpList-Class.md)