---
title: "CListCtrl::GetOutlineColor"
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
ms.assetid: d3e9e34f-4979-4663-8d87-8d2eaf485612
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetOutlineColor
Retrieves the color of the border of a list view control.  
  
## Syntax  
  
```  
  
COLORREF GetOutlineColor( ) const;  
  
```  
  
## Return Value  
 Returns a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) structure containing the outline color.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETOUTLINECOLOR](http://msdn.microsoft.com/library/windows/desktop/bb761065) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)