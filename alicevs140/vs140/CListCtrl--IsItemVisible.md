---
title: "CListCtrl::IsItemVisible"
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
ms.assetid: aa0995c0-fbfa-4bc3-8995-8a3154f74546
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::IsItemVisible
Indicates whether a specified item in the current list-view control is visible.  
  
## Syntax  
  
```  
BOOL IsItemVisible(  
     int index  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `index`|Zero-based index of an item in the current list-view control.|  
  
## Return Value  
 `true` if the specified item is visible;otherwise, `false`.  
  
## Remarks  
 This method sends the [LVM_ISITEMVISIBLE](http://msdn.microsoft.com/library/windows/desktop/bb761135) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_ISITEMVISIBLE](http://msdn.microsoft.com/library/windows/desktop/bb761135)