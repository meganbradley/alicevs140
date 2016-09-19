---
title: "CTreeCtrl::GetItemStateEx"
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
ms.assetid: 43ed8ce0-7d83-48e9-abbc-732c9b6b5209
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItemStateEx
Retrieves the extended state of the specified item in the current tree-view control.  
  
## Syntax  
  
```  
UINT GetItemStateEx(  
     HTREEITEM hItem  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `hItem`|Handle to a tree-view control item.|  
  
## Return Value  
 The extended state of the item. For more information, see the `uStateEx` member of the [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459) structure.  
  
## Remarks  
 This method sends the [TVM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb773596) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. That message returns the [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459) structure that describes the tree-view control item, and this method retrieves the `uStateEx` member from that structure.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetItemStateEx](../vs140/CTreeCtrl--SetItemStateEx.md)   
 [TVM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb773596)   
 [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459)