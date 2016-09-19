---
title: "CListCtrl::MoveItemToGroup"
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
ms.assetid: 124a649a-b898-4c1b-8fc9-f8b338522cc0
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::MoveItemToGroup
Moves the specified item into the specified group.  
  
## Syntax  
  
```  
void MoveItemToGroup(  
   int idItemFrom,  
   int idGroupTo  
);  
```  
  
#### Parameters  
 [in] `idItemFrom`  
 The index of the item to be moved.  
  
 [in] `idGroupTo`  
 The identifier of the group the item will be moved to.  
  
## Remarks  
  
> [!NOTE]
>  This method currently is not implemented.  
  
 This method emulates the functionality of the [LVM_MOVEITEMTOGROUP](http://msdn.microsoft.com/library/windows/desktop/bb761143) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)