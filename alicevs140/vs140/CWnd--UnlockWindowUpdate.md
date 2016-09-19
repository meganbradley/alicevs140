---
title: "CWnd::UnlockWindowUpdate"
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
ms.assetid: a8bb5380-3d8b-465a-afde-5a8ca1b9def9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::UnlockWindowUpdate
Call this member function to unlock a window that was locked with `CWnd::LockWindowUpdate`.  
  
## Syntax  
  
```  
  
void UnlockWindowUpdate();  
  
```  
  
## Remarks  
 Only one window at a time can be locked using `LockWindowUpdate`. See [CWnd::LockWindowUpdate](../vs140/CWnd--LockWindowUpdate.md) or the Win32 function [LockWindowUpdate](http://msdn.microsoft.com/library/windows/desktop/dd145034) for more information on locking windows.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)