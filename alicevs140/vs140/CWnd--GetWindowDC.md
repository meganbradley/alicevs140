---
title: "CWnd::GetWindowDC"
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
ms.assetid: 5f27e471-7e81-4f72-bcda-d9cda846155f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetWindowDC
Retrieves the display context for the entire window, including caption bar, menus, and scroll bars.  
  
## Syntax  
  
```  
  
CDC* GetWindowDC( );  
```  
  
## Return Value  
 Identifies the display context for the given window if the function is successful; otherwise **NULL**.  
  
 The returned pointer may be temporary and should not be stored for later use. [ReleaseDC](../vs140/CWnd--ReleaseDC.md) should be called once for each successful call to `GetWindowDC`.  
  
## Remarks  
 A window display context permits painting anywhere in `CWnd`, since the origin of the context is the upper-left corner of `CWnd` instead of the client area.  
  
 Default attributes are assigned to the display context each time it retrieves the context. Previous attributes are lost.  
  
 `GetWindowDC` is intended to be used for special painting effects within the `CWnd` nonclient area. Painting in nonclient areas of any window is not recommended.  
  
 The [GetSystemMetrics](http://msdn.microsoft.com/library/windows/desktop/ms724385) Windows function can be used to retrieve the dimensions of various parts of the nonclient area, such as the caption bar, menu, and scroll bars.  
  
 After painting is complete, the [ReleaseDC](../vs140/CWnd--ReleaseDC.md) member function must be called to release the display context. Failure to release the display context will seriously affect painting requested by applications due to limitations on the number of device contexts that can be open at the same time.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetSystemMetrics](http://msdn.microsoft.com/library/windows/desktop/ms724385)   
 [CWnd::ReleaseDC](../vs140/CWnd--ReleaseDC.md)   
 [GetWindowDC](http://msdn.microsoft.com/library/windows/desktop/dd144947)   
 [CWnd::GetDC](../vs140/CWnd--GetDC.md)   
 [CWindowDC Class](../vs140/CWindowDC-Class.md)