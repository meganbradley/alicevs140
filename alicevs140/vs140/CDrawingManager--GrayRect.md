---
title: "CDrawingManager::GrayRect"
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
ms.assetid: 968e61cb-c3c5-4dfd-a4b9-ef6450cc85d1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::GrayRect
Fills a rectangle with a specified gray color.  
  
## Syntax  
  
```  
BOOL GrayRect(  
   CRect rect,  
   int nPercentage = -1,  
   COLORREF clrTransparent = (COLORREF)-1,  
   COLORREF clrDisabled = (COLORREF)-1  
);  
```  
  
#### Parameters  
 [in] `rect`  
 The rectangular area to fill.  
  
 [in] `nPercentage`  
 The percentage of gray you want in the rectangle.  
  
 [in] `clrTransparent`  
 The transparent color.  
  
 [in] `clrDisabled`  
 The color that this method uses for de-saturation if `nPercentage` is set to -1.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise `FALSE`.  
  
## Remarks  
 For the parameter `nPercentage`, a lower value indicates a darker color.  
  
 The maximum value for `nPercentage` is 200. A value larger than 200 does not change the appearance of the rectangle. If the value is -1, this method uses `clrDisabled` to limit the saturation of the rectangle.  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)