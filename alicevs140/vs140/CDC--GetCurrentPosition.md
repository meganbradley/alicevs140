---
title: "CDC::GetCurrentPosition"
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
ms.assetid: fb8888d3-a207-424a-9a96-b8340a3f2f73
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetCurrentPosition
Retrieves the current position (in logical coordinates).  
  
## Syntax  
  
```  
  
CPoint GetCurrentPosition( ) const;  
```  
  
## Return Value  
 The current position as a `CPoint` object.  
  
## Remarks  
 The current position can be set with the `MoveTo` member function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::MoveTo](../vs140/CDC--MoveTo.md)   
 [CPoint Class](../vs140/CPoint-Class.md)