---
title: "CListCtrl::SetHoverTime"
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
ms.assetid: 1b741396-2892-499b-b7af-42b1cd4d387a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetHoverTime
Sets the current hover time of a list view control.  
  
## Syntax  
  
```  
  
      DWORD SetHoverTime(  
   DWORD dwHoverTime = (DWORD  
)-1   
);  
```  
  
#### Parameters  
 *dwHoverTime*  
 The new delay, in milliseconds, which the mouse cursor must hover over an item before it is selected. If the default value is passed, the time is set to the default hover time.  
  
## Return Value  
 The previous hover time, in milliseconds.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro, [ListView_SetHoverTime](http://msdn.microsoft.com/library/windows/desktop/bb775084), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CListCtrl::GetHoverTime](../vs140/CListCtrl--GetHoverTime.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetHoverTime](../vs140/CListCtrl--GetHoverTime.md)