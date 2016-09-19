---
title: "CListCtrl::SetTileViewInfo"
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
ms.assetid: 91e37826-c065-45b2-8f8e-969658b033b3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetTileViewInfo
Sets information that a list view control uses in tile view.  
  
## Syntax  
  
```  
  
      BOOL SetTileViewInfo(  
   PLVTILEVIEWINFO ptvi   
);  
```  
  
#### Parameters  
 `ptvi`  
 A pointer to an [LVTILEVIEWINFO](http://msdn.microsoft.com/library/windows/desktop/bb774768) structure containing the information to set.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_SETTILEVIEWINFO](http://msdn.microsoft.com/library/windows/desktop/bb761212) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)