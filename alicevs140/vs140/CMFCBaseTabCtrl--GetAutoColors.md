---
title: "CMFCBaseTabCtrl::GetAutoColors"
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
ms.assetid: 9507b2f1-c876-4fc1-ae1f-24e546ae9699
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetAutoColors
Retrieves the array of colors used for automatic coloring.  
  
## Syntax  
  
```  
const CArray<COLORREF,COLORREF>& GetAutoColors() const;  
```  
  
## Return Value  
 A reference to an array of [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) values that the [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md) object uses for automatic tab coloring.  
  
## Remarks  
 By default, the framework initializes the array of colors to library-defined colors. You can provide a custom array of colors by calling the method [CMFCBaseTabCtrl::SetAutoColors](../vs140/CMFCBaseTabCtrl--SetAutoColors.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::EnableAutoColor](../vs140/CMFCBaseTabCtrl--EnableAutoColor.md)   
 [CMFCBaseTabCtrl::SetAutoColors](../vs140/CMFCBaseTabCtrl--SetAutoColors.md)