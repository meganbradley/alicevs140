---
title: "CWnd::DragDetect"
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
ms.assetid: 0c94dd3f-3e5d-4467-8210-32104a4ad97a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::DragDetect
Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.  
  
## Syntax  
  
```  
  
      BOOL DragDetect(  
   POINT pt  
) const;  
```  
  
#### Parameters  
 `pt`  
 Initial position of the mouse, in screen coordinates. The function determines the coordinates of the drag rectangle by using this point.  
  
## Return Value  
 If the user moved the mouse outside of the drag rectangle while holding down the left button , the return value is nonzero.  
  
 If the user did not move the mouse outside of the drag rectangle while holding down the left button , the return value is zero.  
  
## Remarks  
 This member function emulates the functionality of the function [DragDetect](http://msdn.microsoft.com/library/windows/desktop/ms646256), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)