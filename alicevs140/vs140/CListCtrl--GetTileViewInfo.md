---
title: "CListCtrl::GetTileViewInfo"
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
ms.assetid: 6cf38ed9-6b4a-4b39-b5e2-9197accc66a7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetTileViewInfo
Retrieves information about a list view control in tile view.  
  
## Syntax  
  
```  
  
      BOOL GetTileViewInfo(  
   PLVTILEVIEWINFO ptvi   
) const;  
```  
  
#### Parameters  
 `ptvi`  
 A pointer to an [LVTILEVIEWINFO](http://msdn.microsoft.com/library/windows/desktop/bb774768) structure that receives the retrieved information.  
  
## Return Value  
 The return value is not used.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETTILEVIEWINFO](http://msdn.microsoft.com/library/windows/desktop/bb761083) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)