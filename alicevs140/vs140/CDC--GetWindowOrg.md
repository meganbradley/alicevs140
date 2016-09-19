---
title: "CDC::GetWindowOrg"
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
ms.assetid: f12d84ad-9bd9-4331-a403-9e5da503884c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetWindowOrg
Retrieves the x- and y-coordinates of the origin of the window associated with the device context.  
  
## Syntax  
  
```  
  
CPoint GetWindowOrg( ) const;  
```  
  
## Return Value  
 The origin of the window (in logical coordinates) as a `CPoint` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetViewportOrg](../vs140/CDC--GetViewportOrg.md)   
 [CDC::SetWindowOrg](../vs140/CDC--SetWindowOrg.md)   
 [CPoint Class](../vs140/CPoint-Class.md)