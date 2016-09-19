---
title: "CListCtrl::IsGroupViewEnabled"
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
ms.assetid: f237560c-97c4-40e6-a1d7-8672e7ad77f9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::IsGroupViewEnabled
Determines whether group view is enabled for a list view control.  
  
## Syntax  
  
```  
  
BOOL IsGroupViewEnabled( ) const;  
  
```  
  
## Return Value  
 Returns **TRUE** if group view is enabled, or **FALSE** otherwise.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_ISGROUPVIEWENABLED](http://msdn.microsoft.com/library/windows/desktop/bb761133) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)