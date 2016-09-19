---
title: "CD2DPointF Class"
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
ms.assetid: 30f72083-1c8a-4f50-adb2-72dbbe3522d4
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DPointF Class
A wrapper for `D2D1_POINT_2F`.  
  
## Syntax  
  
```  
class CD2DPointF : public D2D1_POINT_2F;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DPointF::CD2DPointF](#cd2dpointf__cd2dpointf)|Overloaded. Constructs a `CD2DPointF` object from `D2D1_POINT_2F` object.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DPointF::operator CPoint](#cd2dpointf__operator_cpoint)|Converts `CD2DPointF` to `CPoint` object.|  
  
## Inheritance Hierarchy  
 `D2D1_POINT_2F`  
  
 [CD2DPointF](../vs140/CD2DPointF-Class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="cd2dpointf__cd2dpointf"></a>  CD2DPointF::CD2DPointF  
 Constructs a CD2DPointF object from CPoint object.  
  
```  
CD2DPointF(  
   const CPoint& pt  
);  
CD2DPointF(  
   const D2D1_POINT_2F& pt  
);  
CD2DPointF(  
   const D2D1_POINT_2F* pt  
);  
CD2DPointF(  
   FLOAT fX = 0.,  
   FLOAT fY = 0.  
);  
```  
  
### Parameters  
 `pt`  
 source point  
  
 `fX`  
 source X  
  
 `fY`  
 source Y  
  
##  <a name="cd2dpointf__operator_cpoint"></a>  CD2DPointF::operator CPoint  
 Converts CD2DPointF to CPoint object.  
  
```  
operator CPoint();  
```  
  
### Return Value  
 Current value of D2D point.  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)