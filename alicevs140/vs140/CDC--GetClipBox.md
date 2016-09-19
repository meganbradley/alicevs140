---
title: "CDC::GetClipBox"
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
ms.assetid: 50c825a9-4af1-452b-82b6-029c32c89ae7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetClipBox
Retrieves the dimensions of the tightest bounding rectangle around the current clipping boundary.  
  
## Syntax  
  
```  
  
      virtual int GetClipBox(  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpRect`  
 Points to the [RECT](../vs140/RECT-Structure.md) structure or [CRect](../vs140/CRect-Class.md) object that is to receive the rectangle dimensions.  
  
## Return Value  
 The clipping region's type. It can be any of the following values:  
  
-   **COMPLEXREGION** Clipping region has overlapping borders.  
  
-   **ERROR** Device context is not valid.  
  
-   **NULLREGION** Clipping region is empty.  
  
-   **SIMPLEREGION** Clipping region has no overlapping borders.  
  
## Remarks  
 The dimensions are copied to the buffer pointed to by `lpRect`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SelectClipRgn](../vs140/CDC--SelectClipRgn.md)   
 [GetClipBox](http://msdn.microsoft.com/library/windows/desktop/dd144865)   
 [RECT Structure](../vs140/RECT-Structure.md)