---
title: "CListCtrl::SetItemIndexState"
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
ms.assetid: ec2ebe55-4dfc-4899-8aba-8752a7de51ae
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetItemIndexState
Sets the state of an item in the current list-view control.  
  
## Syntax  
  
```  
BOOL SetItemIndexState(  
     PLVITEMINDEX pItemIndex,   
     DWORD dwState,   
     DWORD dwMask  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pItemIndex`|Pointer to an [LVITEMINDEX](http://msdn.microsoft.com/library/windows/desktop/bb774762) structure that describes an item. The caller is responsible for allocating this structure and setting its members.|  
|[in] `dwState`|The state to set the item, which is a bitwise combination of [list view item states](http://msdn.microsoft.com/library/windows/desktop/bb774733). Specify zero to reset, or one to set, a state.|  
|[in] `dwMask`|A mask of the valid bits of the state specified by the `dwState` parameter. Specify a bitwise combination (OR) of [list view item states](http://msdn.microsoft.com/library/windows/desktop/bb774733).|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 For more information about the `dwState` parameter, see [List View Item States](http://msdn.microsoft.com/library/windows/desktop/bb774733).  
  
 For more information about the `dwMask` parameter, see the `stateMask` member of the [LVITEM](http://msdn.microsoft.com/library/windows/desktop/bb774760) structure.  
  
 This method sends the [LVM_SETITEMINDEXSTATE](http://msdn.microsoft.com/library/windows/desktop/bb761190) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_SETITEMINDEXSTATE](http://msdn.microsoft.com/library/windows/desktop/bb761190)   
 [LVITEMINDEX](http://msdn.microsoft.com/library/windows/desktop/bb774762)   
 [LVITEM](http://msdn.microsoft.com/library/windows/desktop/bb774760)   
 [List View Item States](http://msdn.microsoft.com/library/windows/desktop/bb774733)