---
title: "CListCtrl::SetOutlineColor"
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
ms.assetid: 3039fb8f-b2f3-4839-9d54-2cbf82ffeba2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetOutlineColor
Sets the color of the border of a list-view control if the [LVS_EX_BORDERSELECT](http://msdn.microsoft.com/library/windows/desktop/bb774739) extended window style is set.  
  
## Syntax  
  
```  
  
      COLORREF SetOutlineColor(  
   COLORREF color   
);  
```  
  
#### Parameters  
 `color`  
 The new [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) structure containing the outline color.  
  
## Return Value  
 The previous **COLORREF** structure containing the outline color  
  
## Remarks  
 This member function emulates the functionality of the [LVM_SETOUTLINECOLOR](http://msdn.microsoft.com/library/windows/desktop/bb761200) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)