---
title: "CWindow::LockWindowUpdate"
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
ms.assetid: ba808bd0-ee91-424c-aa5b-67a1af60b6a3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::LockWindowUpdate
Disables or enables drawing in the window by calling the [LockWindowUpdate](http://msdn.microsoft.com/library/windows/desktop/dd145034) Win32 function.  
  
## Syntax  
  
```  
  
      BOOL LockWindowUpdate(  
   BOOL bLock = TRUE   
) throw();  
```  
  
#### Parameters  
 `bLock`  
 [in] If **TRUE** (the default value), the window will be locked. Otherwise, it will be unlocked.  
  
## Return Value  
 **TRUE** if the window is successfully locked; otherwise, **FALSE**.  
  
## Remarks  
 If `bLock` is **TRUE**, this method passes [m_hWnd](../vs140/CWindow--m_hWnd.md) to the Win32 function; otherwise, it passes **NULL**.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)