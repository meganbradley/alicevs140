---
title: "CListCtrl::GetNextItemIndex"
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
ms.assetid: 5544bec5-ea82-4d6d-8731-426a1e21ecdb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetNextItemIndex
Retrieves the index of the item in the current list-view control that has a specified set of properties.  
  
## Syntax  
  
```  
BOOL GetNextItemIndex(  
     PLVITEMINDEX pItemIndex,   
     int nFlags  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in, out] `pItemIndex`|Pointer to the [LVITEMINDEX](http://msdn.microsoft.com/library/windows/desktop/bb774762) structure that describes the item where the search begins, or -1 to find the first item that matches the flags in the `nFlags` parameter.<br /><br /> If this method is successful, the `LVITEMINDEX` structure describes the item found by the search.|  
|[in] `nFlags`|A bitwise combination (OR) of flags that specify how to perform the search.<br /><br /> The search can depend on the index, state, or appearance of the target item, or the target item's physical position relative to the item specified by the `pItemIndex` parameter. For more information, see the `flags` parameter in the [LVM_GETNEXTITEMINDEX](http://msdn.microsoft.com/library/windows/desktop/bb761059) message.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 The caller is responsible for allocating and setting the members of the `LVITEMINDEX` structure pointed to by the `pItemIndex` parameter.  
  
 This method sends the [LVM_GETNEXTITEMINDEX](http://msdn.microsoft.com/library/windows/desktop/bb761059) message, which is described in the Windows SDK.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_GETNEXTITEMINDEX](http://msdn.microsoft.com/library/windows/desktop/bb761059)   
 [LVITEMINDEX](http://msdn.microsoft.com/library/windows/desktop/bb774762)