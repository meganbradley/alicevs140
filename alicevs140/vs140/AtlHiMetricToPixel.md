---
title: "AtlHiMetricToPixel"
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
ms.assetid: 00c3af58-7298-4082-9a2e-5b68a8cec6fd
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlHiMetricToPixel
Converts an object's size in HIMETRIC units (each unit is 0.01 millimeter) to a size in pixels on the screen device.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      extern void AtlHiMetricToPixel(  
const SIZEL* lpSizeInHiMetric,  
LPSIZEL lpSizeInPix   
);  
```  
  
#### Parameters  
 `lpSizeInHiMetric`  
 [in] Pointer to the size of the object in HIMETRIC units.  
  
 `lpSizeInPix`  
 [out] Pointer to where the object's size in pixels is to be returned.  
  
## Example  
 [!CODE [NVC_ATL_COM#49](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#49)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [AtlPixelToHiMetric](../vs140/AtlPixelToHiMetric.md)   
 [Pixel/HIMETRIC Conversion Global Functions](../vs140/Pixel-HIMETRIC-Conversion-Global-Functions.md)