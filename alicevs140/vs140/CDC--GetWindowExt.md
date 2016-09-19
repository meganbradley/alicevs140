---
title: "CDC::GetWindowExt"
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
ms.assetid: aab8812d-a2e0-4c4b-83c1-a531dbb553ad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetWindowExt
Retrieves the x- and y-extents of the window associated with the device context.  
  
## Syntax  
  
```  
  
CSize GetWindowExt( ) const;  
```  
  
## Return Value  
 The x- and y-extents (in logical units) as a `CSize` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetWindowExt](../vs140/CDC--SetWindowExt.md)   
 [CSize Class](../vs140/CSize-Class.md)   
 [CDC::GetViewportExt](../vs140/CDC--GetViewportExt.md)