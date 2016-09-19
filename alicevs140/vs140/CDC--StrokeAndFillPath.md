---
title: "CDC::StrokeAndFillPath"
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
ms.assetid: 581e12ed-4ebc-42cd-9682-55260778ef19
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::StrokeAndFillPath
Closes any open figures in a path, strokes the outline of the path by using the current pen, and fills its interior by using the current brush.  
  
## Syntax  
  
```  
  
BOOL StrokeAndFillPath( );  
```  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The device context must contain a closed path. The `StrokeAndFillPath` member function has the same effect as closing all the open figures in the path, and stroking and filling the path separately, except that the filled region will not overlap the stroked region even if the pen is wide.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::BeginPath](../vs140/CDC--BeginPath.md)   
 [CDC::FillPath](../vs140/CDC--FillPath.md)   
 [CDC::SetPolyFillMode](../vs140/CDC--SetPolyFillMode.md)   
 [CDC::StrokePath](../vs140/CDC--StrokePath.md)   
 [StrokeAndFillPath](http://msdn.microsoft.com/library/windows/desktop/dd145123)