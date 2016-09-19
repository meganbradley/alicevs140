---
title: "CDrawingManager::RGBtoHSL"
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
ms.assetid: 5a0711e7-7fd5-41aa-aa34-19b37ccaba77
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::RGBtoHSL
Converts a color from a red, green, and blue (RGB) representation to a hue, saturation, and lightness (HSL) representation.  
  
## Syntax  
  
```  
static void __stdcall RGBtoHSL(  
   COLORREF rgb,  
   double *H,  
   double *S,  
   double *L  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `rgb`|The color in RGB values.|  
|[out] `H`|A pointer to a double where the method stores the hue for the color.|  
|[out] `S`|A pointer to a double where the method stores the saturation for the color.|  
|[out] `L`|A pointer to a double where the method stores the lightness for the color.|  
  
## Remarks  
 A color can be represented as HSV (hue, saturation, and value), HSL (hue, saturation, and luminosity), or RGB (red, green, and blue). For more information about the different representations of color, see [Color](http://go.microsoft.com/fwlink/?LinkID=119126).  
  
 The returned value for `H` is represented as a fraction between 0 and 1 where both 0 and 1 represent red. The returned values for `S` and `L` are numbers between 0 and 1.  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDrawingManager::HLStoRGB_ONE](../vs140/CDrawingManager--HLStoRGB_ONE.md)   
 [CDrawingManager::HLStoRGB_TWO](../vs140/CDrawingManager--HLStoRGB_TWO.md)