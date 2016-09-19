---
title: "CDC::GetNearestColor"
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
ms.assetid: 6204fae3-f439-4434-ae8e-c18448f071b4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetNearestColor
Returns the solid color that best matches a specified logical color.  
  
## Syntax  
  
```  
  
      COLORREF GetNearestColor(  
   COLORREF crColor   
) const;  
```  
  
#### Parameters  
 `crColor`  
 Specifies the color to be matched.  
  
## Return Value  
 An RGB (red, green, blue) color value that defines the solid color closest to the `crColor` value that the device can represent.  
  
## Remarks  
 The given device must be able to represent this color.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetNearestColor](http://msdn.microsoft.com/library/windows/desktop/dd144902)   
 [CPalette::GetNearestPaletteIndex](../vs140/CPalette--GetNearestPaletteIndex.md)