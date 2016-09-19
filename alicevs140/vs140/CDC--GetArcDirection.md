---
title: "CDC::GetArcDirection"
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
ms.assetid: 7de180f5-be03-4b62-87da-33c6e16f375a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetArcDirection
Returns the current arc direction for the device context.  
  
## Syntax  
  
```  
  
int GetArcDirection( ) const;  
```  
  
## Return Value  
 Specifies the current arc direction, if successful. Following are the valid return values:  
  
-   **AD_COUNTERCLOCKWISE** Arcs and rectangles drawn counterclockwise.  
  
-   **AD_CLOCKWISE** Arcs and rectangles drawn clockwise.  
  
 If an error occurs, the return value is zero.  
  
## Remarks  
 Arc and rectangle functions use the arc direction.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetArcDirection](../vs140/CDC--SetArcDirection.md)   
 [GetArcDirection](http://msdn.microsoft.com/library/windows/desktop/dd144848)