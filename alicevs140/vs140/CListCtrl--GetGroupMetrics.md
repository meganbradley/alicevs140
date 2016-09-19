---
title: "CListCtrl::GetGroupMetrics"
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
ms.assetid: aeec9745-41c5-4ea9-b121-12949b018471
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetGroupMetrics
Retrieves the metrics of a group.  
  
## Syntax  
  
```  
  
      void GetGroupMetrics(  
   PLVGROUPMETRICS pGroupMetrics   
) const;  
```  
  
#### Parameters  
 `pGroupMetrics`  
 A pointer to a [LVGROUPMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb774752) containing the group metrics information.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETGROUPMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb774934) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetGroupMetrics](../vs140/CListCtrl--SetGroupMetrics.md)