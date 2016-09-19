---
title: "CLinkCtrl::SetItem"
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
ms.assetid: f7bc3b0b-f2d4-4925-afce-f14666faf19a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::SetItem
Sets the states and attributes of a link control item.  
  
## Syntax  
  
```  
  
      BOOL SetItem(  
   PLITEM pItem  
);  
```  
  
#### Parameters  
 `pItem`  
 A pointer to a [LITEM](http://msdn.microsoft.com/library/windows/desktop/bb760710) structure containing the information to set.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [LM_SETITEM](http://msdn.microsoft.com/library/windows/desktop/bb760724), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::GetItem](../vs140/CLinkCtrl--GetItem.md)   
 [CLinkCtrl::SetItemID](../vs140/CLinkCtrl--SetItemID.md)   
 [CLinkCtrl::SetItemState](../vs140/CLinkCtrl--SetItemState.md)   
 [CLinkCtrl::SetItemUrl](../vs140/CLinkCtrl--SetItemUrl.md)