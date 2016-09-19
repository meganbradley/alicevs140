---
title: "CDrawingManager::RGBtoHSV"
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
ms.assetid: c82ea7a4-0fc5-4690-85b1-9428b882aca7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::RGBtoHSV
Converts a color from a RGB representation to a HSV representation.  
  
## Syntax  
  
```  
static void __stdcall RGBtoHSV(  
   COLORREF rgb,  
   double *H,  
   double *S,  
   double *V  
);  
```  
  
#### Parameters  
 [in] `rgb`  
 The color to convert in a RGB representation.  
  
 [out] `H`  
 A pointer to a double where this method stores the resulting hue for the color.  
  
 [out] `S`  
 A pointer to a double where this method stores the resulting saturation for the color.  
  
 [out] `V`  
 A pointer to a double where this method stores the resulting value for the color.  
  
## Remarks  
 A color can be represented as HSV (hue, saturation, and value), HSL (hue, saturation, and luminosity), or RGB (red, green, and blue). For more information about the different representations of color, see [Color](http://go.microsoft.com/fwlink/?LinkID=119126).  
  
 The returned value for `H` is a number between 0 and 360 where both 0 and 360 indicate red. The return values for `S` and `V` are numbers between 0 and 1.  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDrawingManager::HSVtoRGB](../vs140/CDrawingManager--HSVtoRGB.md)