---
title: "CWnd::GetWindowPlacement"
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
ms.assetid: bffdfc1f-daea-46ca-b484-dc4fbd8caf07
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetWindowPlacement
Retrieves the show state and the normal (restored), minimized, and maximized positions of a window.  
  
## Syntax  
  
```  
  
      BOOL GetWindowPlacement(  
   WINDOWPLACEMENT* lpwndpl   
) const;  
```  
  
#### Parameters  
 `lpwndpl`  
 Points to the `WINDOWPLACEMENT` structure that receives the show state and position information.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The **flags** member of the [WINDOWPLACEMENT](../vs140/WINDOWPLACEMENT-Structure.md) structure retrieved by this function is always 0. If `CWnd` is maximized, the **showCmd** member of `WINDOWPLACEMENT` is **SW_SHOWMAXIMIZED**. If the window is minimized, it is **SW_SHOWMINIMIZED.** It is **SW_SHOWNORMAL** otherwise.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetWindowPlacement](../vs140/CWnd--SetWindowPlacement.md)   
 [GetWindowPlacement](http://msdn.microsoft.com/library/windows/desktop/ms633518)