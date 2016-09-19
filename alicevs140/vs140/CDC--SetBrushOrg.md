---
title: "CDC::SetBrushOrg"
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
ms.assetid: 9568c03a-dcd9-492e-b2a8-3beef5a7dcbe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetBrushOrg
Specifies the origin that GDI will assign to the next brush that the application selects into the device context.  
  
## Syntax  
  
```  
  
      CPoint SetBrushOrg(  
   int x,  
   int y   
);  
CPoint SetBrushOrg(  
   POINT point   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the x-coordinate (in device units) of the new origin. This value must be in the range 0–7.  
  
 *y*  
 Specifies the y-coordinate (in device units) of the new origin. This value must be in the range 0–7.  
  
 `point`  
 Specifies the x- and y-coordinates of the new origin. Each value must be in the range 0–7. You can pass either a **POINT** structure or a `CPoint` object for this parameter.  
  
## Return Value  
 The previous origin of the brush in device units.  
  
## Remarks  
 The default coordinates for the brush origin are (0, 0). To alter the origin of a brush, call the `UnrealizeObject` function for the `CBrush` object, call `SetBrushOrg`, and then call the `SelectObject` member function to select the brush into the device context.  
  
 Do not use `SetBrushOrg` with stock `CBrush` objects.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBrush Class](../vs140/CBrush-Class.md)   
 [CDC::GetBrushOrg](../vs140/CDC--GetBrushOrg.md)   
 [CDC::SelectObject](../vs140/CDC--SelectObject.md)   
 [CGdiObject::UnrealizeObject](../vs140/CGdiObject--UnrealizeObject.md)   
 [POINT Structure](../vs140/POINT-Structure.md)   
 [CPoint Class](../vs140/CPoint-Class.md)