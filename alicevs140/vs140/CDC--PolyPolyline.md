---
title: "CDC::PolyPolyline"
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
ms.assetid: b51ac8e3-2388-40b6-a59f-4247a5e7a106
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PolyPolyline
Draws multiple series of connected line segments.  
  
## Syntax  
  
```  
  
      BOOL PolyPolyline(  
   const POINT* lpPoints,  
   const DWORD* lpPolyPoints,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of structures that contains the vertices of the polylines. The polylines are specified consecutively.  
  
 `lpPolyPoints`  
 Points to an array of variables specifying the number of points in the `lpPoints` array for the corresponding polygon. Each entry must be greater than or equal to 2.  
  
 `nCount`  
 Specifies the total number of counts in the `lpPolyPoints` array.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The line segments are drawn by using the current pen. The figures formed by the segments are not filled. The current position is neither used nor updated by this function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Polyline](../vs140/CDC--Polyline.md)   
 [CDC::PolylineTo](../vs140/CDC--PolylineTo.md)   
 [PolyPolyline](http://msdn.microsoft.com/library/windows/desktop/dd162819)