---
title: "CListCtrl::GetView"
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
ms.assetid: c0ae0066-224f-4793-8b6a-5d0cede932a6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetView
Gets the view of the list view control.  
  
## Syntax  
  
```  
  
DWORD GetView( ) const;  
  
```  
  
## Return Value  
 The current view of the list view control.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_GETVIEW](http://msdn.microsoft.com/library/windows/desktop/bb761091) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::SetView](../vs140/CListCtrl--SetView.md)