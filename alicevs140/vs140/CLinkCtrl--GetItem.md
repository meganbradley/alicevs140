---
title: "CLinkCtrl::GetItem"
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
ms.assetid: d4cb6fef-e9a9-4764-9ba0-cb814e94e1bc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::GetItem
Retrieves the states and attributes of a link control item.  
  
## Syntax  
  
```  
  
      BOOL GetItem(  
   PLITEM pItem  
) const;  
```  
  
#### Parameters  
 `pItem`  
 A pointer to a [LITEM](http://msdn.microsoft.com/library/windows/desktop/bb760710) structure to receive item information.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [LM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb760720), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::SetItem](../vs140/CLinkCtrl--SetItem.md)   
 [CLinkCtrl::GetItemID](../vs140/CLinkCtrl--GetItemID.md)   
 [CLinkCtrl::GetItemState](../vs140/CLinkCtrl--GetItemState.md)   
 [CLinkCtrl::GetItemUrl](../vs140/CLinkCtrl--GetItemUrl.md)