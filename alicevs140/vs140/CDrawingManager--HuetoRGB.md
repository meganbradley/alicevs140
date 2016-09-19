---
title: "CDrawingManager::HuetoRGB"
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
ms.assetid: 4268448d-067e-4973-8bc1-49231a38772f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::HuetoRGB
Converts a hue value to a red, green, or blue component.  
  
## Syntax  
  
```  
static double __stdcall HuetoRGB(  
   double m1,  
   double m2,  
   double h  
);  
  
static BYTE __stdcall HueToRGB(  
   float rm1,  
   float rm2,  
   float rh  
);  
```  
  
#### Parameters  
 [in] `m1`  
 See Remarks.  
  
 [in] `m2`  
 See Remarks.  
  
 [in] `h`  
 See Remarks.  
  
 [in] `rm1`  
 See Remarks.  
  
 [in] `rm2`  
 See Remarks.  
  
 [in] `rh`  
 See Remarks.  
  
## Return Value  
 The individual red, green, or blue component for the provided hue.  
  
## Remarks  
 This method is a helper method that the [CDrawingManager Class](../vs140/CDrawingManager-Class.md) uses to compute the individual red, green, and blue components of a color in a HSV or HSL representation. This method is not designed to be called directly by the programmer. The input parameters are values that depend on the conversion algorithm.  
  
 To convert a HSV or HSL color to a RGB representation, call one of the following methods:  
  
-   [CDrawingManager::HSVtoRGB](../vs140/CDrawingManager--HSVtoRGB.md)  
  
-   [CDrawingManager::HLStoRGB_ONE](../vs140/CDrawingManager--HLStoRGB_ONE.md)  
  
-   [CDrawingManager::HLStoRGB_TWO](../vs140/CDrawingManager--HLStoRGB_TWO.md)  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDrawingManager::HSVtoRGB](../vs140/CDrawingManager--HSVtoRGB.md)   
 [CDrawingManager::HLStoRGB_ONE](../vs140/CDrawingManager--HLStoRGB_ONE.md)   
 [CDrawingManager::HLStoRGB_TWO](../vs140/CDrawingManager--HLStoRGB_TWO.md)