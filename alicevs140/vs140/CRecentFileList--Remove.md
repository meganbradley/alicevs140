---
title: "CRecentFileList::Remove"
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
ms.assetid: d4e619a0-7dba-425c-ab74-63c30481acd3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecentFileList::Remove
Removes a file from the MRU file list.  
  
## Syntax  
  
```  
  
      virtual void Remove(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of the file to be removed from the most recently used (MRU) file list.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CRecentFileList Class](../vs140/CRecentFileList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecentFileList::Add](../vs140/CRecentFileList--Add.md)   
 [CRecentFileList::UpdateMenu](../vs140/CRecentFileList--UpdateMenu.md)