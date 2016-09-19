---
title: "CTreeCtrl::GetItemExpandedImageIndex"
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
ms.assetid: 8ce08381-e45f-43c3-bd4c-e6d434e90514
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetItemExpandedImageIndex
Retrieves the index of the image to display when the specified item of the current tree-view control is in the expanded state.  
  
## Syntax  
  
```  
int GetItemExpandedImageIndex(  
    HTREEITEM hItem  
)const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `hItem`|Handle to a tree-view control item.|  
  
## Return Value  
 The index of the image to display when the specified item is in the expanded state.  
  
## Remarks  
 This method sends the [TVM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb773596) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. That message returns the [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459) structure that describes the tree-view control item, and then this method retrieves the `iExpandedImage` member from that structure.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetItemExpandedImageIndex](../vs140/CTreeCtrl--SetItemExpandedImageIndex.md)   
 [TVM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb773596)   
 [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459)