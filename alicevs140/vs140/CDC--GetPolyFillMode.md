---
title: "CDC::GetPolyFillMode"
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
ms.assetid: 432f6a3a-61b6-4ee6-a72c-62ef327feac4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetPolyFillMode
Retrieves the current polygon-filling mode.  
  
## Syntax  
  
```  
  
int GetPolyFillMode( ) const;  
```  
  
## Return Value  
 The current polygon-filled mode, **ALTERNATE** or **WINDING**, if the function is successful.  
  
## Remarks  
 See the `SetPolyFillMode` member function for a description of the polygon-filling modes.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetPolyFillMode](../vs140/CDC--SetPolyFillMode.md)   
 [GetPolyFillMode](http://msdn.microsoft.com/library/windows/desktop/dd144910)