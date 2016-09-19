---
title: "CMFCPropertyGridCtrl::IsGroupNameFullWidth"
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
ms.assetid: 7715e2c0-7f0a-4308-aa16-f9c24b559bc7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::IsGroupNameFullWidth
Indicates whether each property group name is displayed across the width of the current property grid control.  
  
## Syntax  
  
```  
BOOL IsGroupNameFullWidth() const;  
```  
  
## Return Value  
 `TRUE` if group names are displayed across the width of the property grid control; `FALSE` if group names are truncated by the right (value) column of the control.  
  
## Remarks  
 A *group* is a collection of related properties in a property grid control. If the control is displayed hierarchically, the *group name* is displayed as a category title in the row above the group.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)