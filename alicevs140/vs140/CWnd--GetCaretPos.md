---
title: "CWnd::GetCaretPos"
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
ms.assetid: b6d4e5d3-2720-4ed5-8851-df0473f4618f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetCaretPos
Retrieves the client coordinates of the caret's current position and returns them as a `CPoint`.  
  
## Syntax  
  
```  
  
static CPoint PASCAL GetCaretPos( );  
```  
  
## Return Value  
 [CPoint](../vs140/CPoint-Class.md) object containing the coordinates of the caret's position.  
  
## Remarks  
 The caret position is given in the client coordinates of the `CWnd` window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetCaretPos](http://msdn.microsoft.com/library/windows/desktop/ms648402)