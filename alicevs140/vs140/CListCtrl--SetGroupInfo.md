---
title: "CListCtrl::SetGroupInfo"
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
ms.assetid: 76a0807b-b4c6-4ddf-8a6b-0d12a58ad369
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetGroupInfo
Sets the information that describes the specified group of the current list-view control.  
  
## Syntax  
  
```  
int SetGroupInfo(  
    int iGroupId,  
    PLVGROUP pgrp   
);  
```  
  
#### Parameters  
 `iGroupId`  
 The identifier of the group whose information is set.  
  
 `pgrp`  
 Pointer to an [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769) structure that contains the information to set. The caller is responsible for allocating this structure and setting its members.  
  
## Return Value  
 The ID of the group if the method is successful; otherwise, -1.  
  
## Remarks  
 This method sends the [LVM_SETGROUPINFO](http://msdn.microsoft.com/library/windows/desktop/bb761167) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_SETGROUPINFO](http://msdn.microsoft.com/library/windows/desktop/bb761167)   
 [CListCtrl::GetGroupInfo](../vs140/CListCtrl--GetGroupInfo.md)