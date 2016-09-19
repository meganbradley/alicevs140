---
title: "CWnd::GetSafeHwnd"
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
ms.assetid: 0179bc13-81f7-4c96-97a9-cf15113407c6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetSafeHwnd
Returns `m_hWnd`, or **NULL** if the **this** pointer is **NULL**.  
  
## Syntax  
  
```  
  
HWND GetSafeHwnd( ) const;  
```  
  
## Return Value  
 Returns the window handle for a window. Returns **NULL** if the `CWnd` is not attached to a window or if it is used with a **NULL CWnd** pointer.  
  
## Example  
 See the example for [CWnd::SubclassWindow](../vs140/CWnd--SubclassWindow.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)