---
title: "CDrawingManager::SetPixel"
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
ms.assetid: 43e06c64-c14c-4a8f-8acc-ebc28acf1862
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::SetPixel
Changes a single pixel in a bitmap to the specified color.  
  
## Syntax  
  
```  
static void __stdcall SetPixel(  
   COLORREF* pBits,  
   int cx,  
   int cy,  
   int x,  
   int y,  
   COLORREF color  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pBits`|A pointer to the bit values of the bitmap.|  
|[in] `cx`|The total width of the bitmap.|  
|[in] `cy`|The total height of the bitmap.|  
|[in] `x`|The x-coordinate of the pixel in the bitmap to change.|  
|[in] `y`|The y-coordinate of the pixel in the bitmap to change.|  
|[in] `color`|The new color for the pixel identified by the supplied coordinates.|  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)