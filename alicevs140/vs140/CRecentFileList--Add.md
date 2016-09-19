---
title: "CRecentFileList::Add"
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
ms.assetid: 12f848c9-e543-4a2b-9bd6-7630c6c11684
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecentFileList::Add
Adds a file to the most recently used (MRU) file list.  
  
## Syntax  
  
```  
  
      virtual void Add(  
   LPCTSTR lpszPathName   
);  
virtual void Add(  
   LPCTSTR lpszPathName,  
   LPCTSTR lpszAppID  
);  
void Add(  
   IShellItem* pItem,  
   LPCTSTR lpszAppID  
);  
void Add(  
   IShellLink* pLink,  
   LPCTSTR lpszAppID  
);  
void Add(  
   PIDLIST_ABSOLUTE pidl,  
   LPCTSTR lpszAppID  
);  
  
```  
  
#### Parameters  
 `lpszPathName`  
 Specifies pathname to be added to the list.  
  
 `lpszAppID`  
 Specifies Application User Model ID for the application.  
  
 `pItem`  
 Specifies a pointer to Shell Item to be added to the list.  
  
 `pLink`  
 Specifies a pointer to Shell Link to be added to the list.  
  
 `pidl`  
 Specifies the IDLIST for the shell item that should be added to the recent docs folder.  
  
## Remarks  
 The file name will be added to the top of the MRU list. If the file name already exists in the MRU list, it will be moved to the top.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CRecentFileList Class](../vs140/CRecentFileList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecentFileList::Remove](../vs140/CRecentFileList--Remove.md)   
 [CRecentFileList::UpdateMenu](../vs140/CRecentFileList--UpdateMenu.md)