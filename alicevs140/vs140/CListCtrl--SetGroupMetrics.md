---
title: "CListCtrl::SetGroupMetrics"
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
ms.assetid: 3cd7fad7-c9ae-4fb9-85a8-f20542d484ae
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetGroupMetrics
Sets the group metrics of a list view control.  
  
## Syntax  
  
```  
  
      void SetGroupMetrics(  
   PLVGROUPMETRICS pGroupMetrics   
);  
```  
  
#### Parameters  
 `pGroupMetrics`  
 A pointer to an [LVGROUPMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb774752) structure containing the group metrics information to be set.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_SETGROUPMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb761168) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetGroupMetrics](../vs140/CListCtrl--GetGroupMetrics.md)