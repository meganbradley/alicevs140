---
title: "CListCtrl::GetTileInfo"
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
ms.assetid: 4781dc36-ffaf-4458-9e87-bcd05c421cf4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetTileInfo
Retrieves information about a tile in a list view control.  
  
## Syntax  
  
```  
  
      BOOL GetTileInfo(  
   PLVTILEINFO pti   
) const;  
```  
  
#### Parameters  
 *pti*  
 A pointer to an [LVTILEINFO](http://msdn.microsoft.com/library/windows/desktop/bb774766) structure that receives the tile information.  
  
## Return Value  
 The return value is not used.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETTILEINFO](http://msdn.microsoft.com/library/windows/desktop/bb761081) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)