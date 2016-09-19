---
title: "CTreeCtrl::GetItem"
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
ms.assetid: aa2f7bd6-75e4-4c9e-81a4-b858bdd4b5f8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItem
Call this function to retrieve the attributes of the specified tree view item.  
  
## Syntax  
  
```  
  
      BOOL GetItem(  
   TVITEM* pItem   
) const;  
```  
  
#### Parameters  
 `pItem`  
 A pointer to a [TVITEM](http://msdn.microsoft.com/library/windows/desktop/bb773456) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 See the example for [CTreeCtrl::DeleteItem](../vs140/CTreeCtrl--DeleteItem.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetItem](../vs140/CTreeCtrl--SetItem.md)   
 [CTreeCtrl::GetChildItem](../vs140/CTreeCtrl--GetChildItem.md)   
 [CTreeCtrl::GetNextItem](../vs140/CTreeCtrl--GetNextItem.md)   
 [CTreeCtrl::SelectItem](../vs140/CTreeCtrl--SelectItem.md)