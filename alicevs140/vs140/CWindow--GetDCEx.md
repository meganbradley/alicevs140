---
title: "CWindow::GetDCEx"
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
ms.assetid: 402521f1-897b-4ff9-bad6-349658fb9c73
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetDCEx
Retrieves a device context for the client area and allows clipping options.  
  
## Syntax  
  
```  
  
      HDC GetDCEx(  
   HRGN hRgnClip,  
   DWORD flags   
) throw();  
```  
  
## Remarks  
 See [GetDCEx](http://msdn.microsoft.com/library/windows/desktop/dd144873) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetDC](../vs140/CWindow--GetDC.md)   
 [CWindow::GetWindowDC](../vs140/CWindow--GetWindowDC.md)   
 [CWindow::ReleaseDC](../vs140/CWindow--ReleaseDC.md)