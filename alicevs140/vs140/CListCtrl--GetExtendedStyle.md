---
title: "CListCtrl::GetExtendedStyle"
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
ms.assetid: 4fe64033-098f-46e9-873b-7738332bbc1d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetExtendedStyle
Retrieves the current extended styles of a list view control.  
  
## Syntax  
  
```  
  
DWORD GetExtendedStyle( );  
  
```  
  
## Return Value  
 A combination of the extended styles currently in use by the list view control. For a descriptive list of these extended styles, see the [Extended List View Styles](http://msdn.microsoft.com/library/windows/desktop/bb774732) topic in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_GetExtendedListViewStyle](http://msdn.microsoft.com/library/windows/desktop/bb761264), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CListCtrl::SetExtendedStyle](../vs140/CListCtrl--SetExtendedStyle.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetExtendedStyle](../vs140/CListCtrl--SetExtendedStyle.md)