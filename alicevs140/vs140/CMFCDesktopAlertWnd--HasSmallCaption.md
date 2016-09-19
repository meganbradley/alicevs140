---
title: "CMFCDesktopAlertWnd::HasSmallCaption"
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
ms.assetid: dd24f906-0b1c-464b-b830-f109f616d2e0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDesktopAlertWnd::HasSmallCaption
Determines whether the desktop alert window has a small caption or a regular-size caption.  
  
## Syntax  
  
```  
BOOL HasSmallCaption() const;  
```  
  
## Return Value  
 `TRUE` if the popup window is displayed with a small caption; `FALSE` if the popup window is displayed with a regular-sized caption.  
  
## Remarks  
 Use this method to determine whether the popup window has a small caption or a regular-size caption. By default, the small caption is 7 pixels high. You can obtain the height of the regular-size caption by calling the Windows API function `GetSystemMetrics(SM_CYCAPTION)`.  
  
## Requirements  
 **Header:** afxDesktopAlertWnd.h  
  
## See Also  
 [CMFCDesktopAlertWnd Class](../vs140/CMFCDesktopAlertWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)