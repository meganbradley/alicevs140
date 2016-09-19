---
title: "CListCtrl::GetGroupState"
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
ms.assetid: 3d496073-989c-4247-962b-c4c2b84bb651
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetGroupState
Retrieves the state for a specified group in the current list-view control.  
  
## Syntax  
  
```  
UINT GetGroupState(  
     int iGroupId,   
     DWORD dwMask  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iGroupId`|Zero-based index of a group.|  
|[in] `dwMask`|Mask that specifies the state value to retrieve for the specified group. For more information, see the `mask` member of the [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769) structure.|  
  
## Return Value  
 The requested state for the specified group, or 0 if the group cannot be found.  
  
## Remarks  
 The return value is the result of a bitwise AND operation on the `dwMask` parameter and the value of the `state` member of an [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769) structure that represents the current list-view control.  
  
 This method sends the [LVM_GETGROUPSTATE](http://msdn.microsoft.com/library/windows/desktop/bb774936) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information, see the [ListView_GetGroupState](http://msdn.microsoft.com/library/windows/desktop/bb761288) macro.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_GETGROUPSTATE](http://msdn.microsoft.com/library/windows/desktop/bb774936)   
 [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769)   
 [ListView_GetGroupState](http://msdn.microsoft.com/library/windows/desktop/bb761288)