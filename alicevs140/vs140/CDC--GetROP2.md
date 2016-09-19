---
title: "CDC::GetROP2"
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
ms.assetid: 2e1e4339-fa54-40c8-9a9a-9e0e81159788
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetROP2
Retrieves the current drawing mode.  
  
## Syntax  
  
```  
  
int GetROP2( ) const;  
```  
  
## Return Value  
 The drawing mode. For a list of the drawing mode values, see the `SetROP2` member function.  
  
## Remarks  
 The drawing mode specifies how the colors of the pen and the interior of filled objects are combined with the color already on the display surface.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetDeviceCaps](../vs140/CDC--GetDeviceCaps.md)   
 [CDC::SetROP2](../vs140/CDC--SetROP2.md)   
 [GetROP2](http://msdn.microsoft.com/library/windows/desktop/dd144922)