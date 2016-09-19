---
title: "CLinkCtrl::SetItemState"
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
ms.assetid: 392eb272-f092-4623-9b11-c8a33403dd4c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::SetItemState
Retrieves the state of the link control item.  
  
## Syntax  
  
```  
  
      BOOL SetItemState(  
   int iLink,  
   UINT state,  
   UINT stateMask = LIS_FOCUSED | LIS_ENABLED | LIS_VISITED   
);  
```  
  
#### Parameters  
 `iLink`  
 The index of a link control item.  
  
 `pnState`  
 The value of the specified state item being set.  
  
 `stateMask`  
 Combination of flags describing the state item being set. For a list of values, see the description of the **state** member in the [LITEM](http://msdn.microsoft.com/library/windows/desktop/bb760710) structure. Allowable items are identical to those allowed in **state**.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 Sets the value of the specified state item of a specific link control item. For more information, see the Win32 message [LM_SETITEM](http://msdn.microsoft.com/library/windows/desktop/bb760724) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CLinkCtrl::GetItemState](../vs140/CLinkCtrl--GetItemState.md)   
 [CLinkCtrl::GetItem](../vs140/CLinkCtrl--GetItem.md)