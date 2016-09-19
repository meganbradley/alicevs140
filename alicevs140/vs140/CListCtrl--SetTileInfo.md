---
title: "CListCtrl::SetTileInfo"
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
ms.assetid: fc88278e-897e-4d35-a902-b0503c7b78aa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetTileInfo
Sets the information for a tile of the list view control.  
  
## Syntax  
  
```  
  
      BOOL SetTileInfo(  
   PLVTILEINFO pti   
);  
```  
  
#### Parameters  
 *pti*  
 A pointer to an [LVTILEINFO](http://msdn.microsoft.com/library/windows/desktop/bb774766) structure containing the information to be set.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_SETTILEINFO](http://msdn.microsoft.com/library/windows/desktop/bb761210) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetTileInfo](../vs140/CListCtrl--GetTileInfo.md)