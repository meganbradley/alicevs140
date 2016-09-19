---
title: "CD2DRectF Class"
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
ms.assetid: 87c12d87-9d18-4a19-ba14-0f51d6b6835a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DRectF Class
A wrapper for `D2D1_RECT_F`.  
  
## Syntax  
  
```  
class CD2DRectF : public D2D1_RECT_F;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DRectF::CD2DRectF](#cd2drectf__cd2drectf)|Overloaded. Constructs a `CD2DRectF` object from `D2D1_RECT_F` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DRectF::IsNull](#cd2drectf__isnull)|Returns a `boolean` value that indicates whether an expression contains no valid data ( `null`).|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DRectF::operator CRect](#cd2drectf__operator_crect)|Converts `CD2DRectF` to `CRect` object.|  
  
## Inheritance Hierarchy  
 `D2D1_RECT_F`  
  
 [CD2DRectF](../vs140/CD2DRectF-Class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="cd2drectf__cd2drectf"></a>  CD2DRectF::CD2DRectF  
 Constructs a CD2DRectF object from CRect object.  
  
```  
CD2DRectF(  
   const CRect& rect  
);  
CD2DRectF(  
   const D2D1_RECT_F& rect  
);  
CD2DRectF(  
   const D2D1_RECT_F* rect  
);  
CD2DRectF(  
   FLOAT fLeft = 0.,  
   FLOAT fTop = 0.,  
   FLOAT fRight = 0.,  
   FLOAT fBottom = 0.  
);  
```  
  
### Parameters  
 `rect`  
 source rectangle  
  
 `fLeft`  
 source left coordinate  
  
 `fTop`  
 source top coordinate  
  
 `fRight`  
 source right coordinate  
  
 `fBottom`  
 source bottom coordinate  
  
##  <a name="cd2drectf__isnull"></a>  CD2DRectF::IsNull  
 Returns a Boolean value that indicates whether an expression contains no valid data (Null).  
  
```  
BOOL IsNull() const;  
```  
  
### Return Value  
 TRUE if rectangle's top, left, bottom, and right values are all equal to 0; otherwise FALSE.  
  
##  <a name="cd2drectf__operator_crect"></a>  CD2DRectF::operator CRect  
 Converts CD2DRectF to CRect object.  
  
```  
operator CRect();  
```  
  
### Return Value  
 Current value of D2D rectangle.  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)