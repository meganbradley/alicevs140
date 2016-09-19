---
title: "CDC::GetWindow"
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
ms.assetid: b22663fe-81a0-4145-a4c1-87b6939c81e6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetWindow
Returns the window associated with the display device context.  
  
## Syntax  
  
```  
  
CWnd* GetWindow( ) const;  
```  
  
## Return Value  
 Pointer to a `CWnd` object if successful; otherwise **NULL**.  
  
## Remarks  
 This is an advanced function. For example, this member function may not return the view window when printing or in print preview. It always returns the window associated with output. Output functions that use the given DC draw into this window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDC](../vs140/CWnd--GetDC.md)   
 [CWnd::GetWindowDC](../vs140/CWnd--GetWindowDC.md)   
 [GetWindow](http://msdn.microsoft.com/library/windows/desktop/ms633515)