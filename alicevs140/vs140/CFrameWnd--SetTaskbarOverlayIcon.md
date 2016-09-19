---
title: "CFrameWnd::SetTaskbarOverlayIcon"
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
ms.assetid: de01645d-99ac-4a35-8bd6-f1047c9975d3
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::SetTaskbarOverlayIcon
Overloaded. Applies an overlay to a taskbar button to indicate application status or to notify the user.  
  
## Syntax  
  
```  
BOOL SetTaskbarOverlayIcon(  
   UINT nIDResource,  
   LPCTSTR lpcszDescr  
);  
BOOL SetTaskbarOverlayIcon(  
   HICON hIcon,  
   LPCTSTR lpcszDescr  
);  
```  
  
#### Parameters  
 `nIDResource`  
 Specifies the Resource ID of an icon to use as the overlay. See description for `hIcon` for details.  
  
 `lpcszDescr`  
 A pointer to a string that provides an alt text version of the information conveyed by the overlay, for accessibility purposes.  
  
 `hIcon`  
 The handle of an icon to use as the overlay. This should be a small icon, measuring 16x16 pixels at 96 dots per inch (dpi). If an overlay icon is already applied to the taskbar button, that existing overlay is replaced. This value can be `NULL`. How a `NULL` value is handled depends on whether the taskbar button represents a single window or a group of windows. It is the responsibility of the calling application to free `hIcon` when it is no longer needed.  
  
## Return Value  
 `TRUE` if successful; `FALSE` if OS version is less than Windows 7 or if an error occurs setting the icon.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)