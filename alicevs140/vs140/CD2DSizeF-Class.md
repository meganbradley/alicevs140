---
title: "CD2DSizeF Class"
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
ms.assetid: f486a1e1-997d-4286-8cb9-26369dc82055
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DSizeF Class
A wrapper for D2D1_SIZE_F.  
  
## Syntax  
  
```  
class CD2DSizeF : public D2D1_SIZE_F;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DSizeF::CD2DSizeF](#cd2dsizef__cd2dsizef)|Overloaded. Constructs a `CD2DSizeF` object from `D2D1_SIZE_F` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DSizeF::IsNull](#cd2dsizef__isnull)|Returns a `boolean` value that indicates whether an expression contains no valid data ( `null`).|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DSizeF::operator CSize](#cd2dsizef__operator_csize)|Converts `CD2DSizeF` to `CSize` object.|  
  
## Inheritance Hierarchy  
 `D2D1_SIZE_F`  
  
 [CD2DSizeF](../vs140/CD2DSizeF-Class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="cd2dsizef__cd2dsizef"></a>  CD2DSizeF::CD2DSizeF  
 Constructs a CD2DSizeF object from CSize object.  
  
```  
CD2DSizeF(  
   const CSize& size  
);  
CD2DSizeF(  
   const D2D1_SIZE_F& size  
);  
CD2DSizeF(  
   const D2D1_SIZE_F* size  
);  
CD2DSizeF(  
   FLOAT cx = 0.,  
   FLOAT cy = 0.  
);  
```  
  
### Parameters  
 `size`  
 source size  
  
 `cx`  
 source width  
  
 `cy`  
 source height  
  
##  <a name="cd2dsizef__isnull"></a>  CD2DSizeF::IsNull  
 Returns a Boolean value that indicates whether an expression contains no valid data (Null).  
  
```  
BOOL IsNull() const;  
```  
  
### Return Value  
 TRUE if width and height are empty; otherwise FALSE.  
  
##  <a name="cd2dsizef__operator_csize"></a>  CD2DSizeF::operator CSize  
 Converts CD2DSizeF to CSize object.  
  
```  
operator CSize();  
```  
  
### Return Value  
 Current value of D2D size.  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)