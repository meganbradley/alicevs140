---
title: "CListCtrl::ApproximateViewRect"
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
ms.assetid: e7b694fd-955d-41d4-a1f5-aef7fe0bcd23
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::ApproximateViewRect
Determines the width and height required to display the items of a list view control.  
  
## Syntax  
  
```  
  
      CSize ApproximateViewRect(  
   CSize sz = CSize(-1,  
   -1  
),  
   int iCount = -1   
) const;  
```  
  
#### Parameters  
 `sz`  
 The proposed dimensions of the control, in pixels. If dimensions are not specified, the framework uses the current width or height values of the control.  
  
 `iCount`  
 Number of items to be displayed in the control. If this parameter is -1, the framework uses the total number of items currently in the control.  
  
## Return Value  
 A `CSize` object that contains the approximate width and height needed to display the items, in pixels.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_ApproximateViewRect](http://msdn.microsoft.com/library/windows/desktop/bb761231), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetViewRect](../vs140/CListCtrl--GetViewRect.md)