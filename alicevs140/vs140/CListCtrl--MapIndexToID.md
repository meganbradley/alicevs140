---
title: "CListCtrl::MapIndexToID"
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
ms.assetid: 2cd20dbe-20d1-40a2-b938-e990cdeea81e
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::MapIndexToID
Maps the index of an item in the current list-view control to a unique ID.  
  
## Syntax  
  
```  
UINT MapIndexToID(  
     UINT index  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `index`|The zero-based index of an item.|  
  
## Return Value  
 A unique ID for the specified item.  
  
## Remarks  
 A list-view control internally tracks items by index. This can present problems because indexes can change during the control's lifetime. The list-view control can tag an item with an ID when the item is created. You can use this ID to access a specific item for the lifetime of the list-view control.  
  
 Note that in a multithreaded environment the index is guaranteed only on the thread that hosts the list-view control, not on background threads.  
  
 This method sends the [LVM_MAPINDEXTOID](http://msdn.microsoft.com/library/windows/desktop/bb761139) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines a variable, `m_listCtrl`, that is used to access the current list-view control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CListCtrl_s2#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl_s2#6)]  
  
## Example  
 The following code example demonstrates the `MapIndexToID` method. In an earlier section of this code example, we created a list-view control that displays two columns titled "ClientID" and "Grade" in a report view. The following example maps the index of each list-view item to an identification number, and then retrieves the index for each identification number. Finally, the example reports whether the original indexes were retrieved.  
  
 [!CODE [NVC_MFC_CListCtrl_s2#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl_s2#3)]  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_MAPINDEXTOID](http://msdn.microsoft.com/library/windows/desktop/bb761139)   
 [CListCtrl::MapIDToIndex](../vs140/CListCtrl--MapIDToIndex.md)