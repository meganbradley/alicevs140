---
title: "CDC::FillPath"
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
ms.assetid: 70f45fc4-09f4-4afd-af50-56a4a165a343
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::FillPath
Closes any open figures in the current path and fills the path's interior by using the current brush and polygon-filling mode.  
  
## Syntax  
  
```  
  
BOOL FillPath( );  
```  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 After its interior is filled, the path is discarded from the device context.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::BeginPath](../vs140/CDC--BeginPath.md)   
 [CDC::SetPolyFillMode](../vs140/CDC--SetPolyFillMode.md)   
 [CDC::StrokeAndFillPath](../vs140/CDC--StrokeAndFillPath.md)   
 [CDC::StrokePath](../vs140/CDC--StrokePath.md)   
 [FillPath](http://msdn.microsoft.com/library/windows/desktop/dd162718)