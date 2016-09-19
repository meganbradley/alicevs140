---
title: "CWnd::SetWindowPlacement"
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
ms.assetid: 4a37d32f-9d57-4f27-82bc-0f5f4c8b8a09
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetWindowPlacement
Sets the show state and the normal (restored), minimized, and maximized positions for a window.  
  
## Syntax  
  
```  
  
      BOOL SetWindowPlacement(  
   const WINDOWPLACEMENT*lpwndpl   
);   
```  
  
#### Parameters  
 `lpwndpl`  
 Points to a [WINDOWPLACEMENT](../vs140/WINDOWPLACEMENT-Structure.md) structure that specifies the new show state and positions.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetWindowPlacement](../vs140/CWnd--GetWindowPlacement.md)   
 [SetWindowPlacement](http://msdn.microsoft.com/library/windows/desktop/ms633544)