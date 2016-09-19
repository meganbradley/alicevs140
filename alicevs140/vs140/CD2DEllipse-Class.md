---
title: "CD2DEllipse Class"
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
ms.assetid: e9f02f54-acf2-427e-b349-db50cd9a77df
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DEllipse Class
A wrapper for `D2D1_ELLIPSE`.  
  
## Syntax  
  
```  
class CD2DEllipse : public D2D1_ELLIPSE;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DEllipse::CD2DEllipse](#cd2dellipse__cd2dellipse)|Overloaded. Constructs a `CD2DEllipse` object from `D2D1_ELLIPSE` object.|  
  
## Inheritance Hierarchy  
 `D2D1_ELLIPSE`  
  
 [CD2DEllipse](../vs140/CD2DEllipse-Class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="cd2dellipse__cd2dellipse"></a>  CD2DEllipse::CD2DEllipse  
 Constructs a CD2DEllipse object from CD2DRectF object.  
  
```  
CD2DEllipse(  
   const CD2DRectF& rect  
);  
CD2DEllipse(  
   const D2D1_ELLIPSE& ellipse  
);  
CD2DEllipse(  
   const D2D1_ELLIPSE* ellipse  
);  
CD2DEllipse(  
   const CD2DPointF& ptCenter,  
   const CD2DSizeF& sizeRadius  
);  
```  
  
### Parameters  
 `rect`  
 source rectangle  
  
 `ellipse`  
 source ellipse  
  
 `ptCenter`  
 The center point of the ellipse.  
  
 `sizeRadius`  
 The X-radius and Y-radius of the ellipse.  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)