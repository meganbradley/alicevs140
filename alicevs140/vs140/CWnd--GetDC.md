---
title: "CWnd::GetDC"
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
ms.assetid: fbace776-e0cf-4928-a057-6a2e739bd86c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetDC
Retrieves a pointer to a common, class, or private device context for the client area depending on the class style specified for the `CWnd`.  
  
## Syntax  
  
```  
  
CDC* GetDC( );  
```  
  
## Return Value  
 Identifies the device context for the `CWnd` client area if successful; otherwise, the return value is **NULL**. The pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 For common device contexts, `GetDC` assigns default attributes to the context each time it is retrieved. For class and private contexts, `GetDC` leaves the previously assigned attributes unchanged. The device context can be used in subsequent graphics device interface (GDI) functions to draw in the client area.  
  
 Unless the device context belongs to a window class, the [ReleaseDC](../vs140/CWnd--ReleaseDC.md) member function must be called to release the context after painting.  
  
 A device context belonging to the `CWnd` class is returned by the `GetDC` member function if **CS_CLASSDC**, **CS_OWNDC**, or **CS_PARENTDC** was specified as a style in the **WNDCLASS** structure when the class was registered.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDCEx](../vs140/CWnd--GetDCEx.md)   
 [CWnd::ReleaseDC](../vs140/CWnd--ReleaseDC.md)   
 [CWnd::GetWindowDC](../vs140/CWnd--GetWindowDC.md)   
 [GetDC](http://msdn.microsoft.com/library/windows/desktop/dd144871)   
 [CClientDC Class](../vs140/CClientDC-Class.md)