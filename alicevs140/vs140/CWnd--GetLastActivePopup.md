---
title: "CWnd::GetLastActivePopup"
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
ms.assetid: ab6f677d-2f44-4fd5-ac69-9ffcc40702c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetLastActivePopup
Determines which pop-up window owned by `CWnd` was most recently active.  
  
## Syntax  
  
```  
  
CWnd* GetLastActivePopup( ) const;  
```  
  
## Return Value  
 Identifies the most recently active pop-up window. The return value will be the window itself if any of the following conditions are met:  
  
-   The window itself was most recently active.  
  
-   The window does not own any pop-up windows.  
  
-   The window is not a top-level window or is owned by another window.  
  
 The pointer may be temporary and should not be stored for later use.  
  
## Example  
 See the example for [CWnd::FindWindow](../vs140/CWnd--FindWindow.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetLastActivePopup](http://msdn.microsoft.com/library/windows/desktop/ms633507)