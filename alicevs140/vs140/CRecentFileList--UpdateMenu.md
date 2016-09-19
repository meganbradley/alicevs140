---
title: "CRecentFileList::UpdateMenu"
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
ms.assetid: a289dd7b-7f39-4685-bc16-08b3a8a198ba
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecentFileList::UpdateMenu
Updates the menu display of the MRU file list.  
  
## Syntax  
  
```  
  
      virtual void UpdateMenu(  
   CCmdUI* pCmdUI   
);  
```  
  
#### Parameters  
 `pCmdUI`  
 A pointer to the [CCmdUI](../vs140/CCmdUI-Class.md) object for the most recently used (MRU) file list menu.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CRecentFileList Class](../vs140/CRecentFileList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecentFileList::Add](../vs140/CRecentFileList--Add.md)   
 [CRecentFileList::Remove](../vs140/CRecentFileList--Remove.md)