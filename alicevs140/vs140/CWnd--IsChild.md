---
title: "CWnd::IsChild"
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
ms.assetid: c02e4a30-446d-433d-a03f-64239bf1f8cd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::IsChild
Indicates whether the window specified by `pWnd` is a child window or other direct descendant of `CWnd`.  
  
## Syntax  
  
```  
  
      BOOL IsChild(  
   const CWnd* pWnd   
) const;  
```  
  
#### Parameters  
 `pWnd`  
 Identifies the window to be tested.  
  
## Return Value  
 Specifies the outcome of the function. The value is nonzero if the window identified by `pWnd` is a child window of `CWnd`; otherwise 0.  
  
## Remarks  
 A child window is the direct descendant of `CWnd` if the `CWnd` object is in the chain of parent windows that leads from the original pop-up window to the child window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IsChild](http://msdn.microsoft.com/library/windows/desktop/ms633524)