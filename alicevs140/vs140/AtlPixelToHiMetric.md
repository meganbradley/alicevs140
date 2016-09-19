---
title: "AtlPixelToHiMetric"
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
ms.assetid: a0bd0c50-7ce9-4c62-9642-bcbd7c79a071
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlPixelToHiMetric
Converts an object's size in pixels on the screen device to a size in HIMETRIC units (each unit is 0.01 millimeter).  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      extern void AtlPixelToHiMetric(  
const SIZEL* lpSizeInPix,  
LPSIZEL lpSizeInHiMetric   
);  
```  
  
#### Parameters  
 `lpSizeInPix`  
 [in] Pointer to the object's size in pixels.  
  
 `lpSizeInHiMetric`  
 [out] Pointer to where the object's size in HIMETRIC units is to be returned.  
  
## Example  
 [!CODE [NVC_ATL_COM#51](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#51)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Pixel/HIMETRIC Conversion Global Functions](../vs140/Pixel-HIMETRIC-Conversion-Global-Functions.md)   
 [AtlHiMetricToPixel](../vs140/AtlHiMetricToPixel.md)