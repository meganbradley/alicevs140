---
title: "CD2DSizeU Class"
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
ms.assetid: 6e679ba8-2112-43c3-8275-70b660856f02
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DSizeU Class
A wrapper for D2D1_SIZE_U.  
  
## Syntax  
  
```  
class CD2DSizeU : public D2D1_SIZE_U;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DSizeU::CD2DSizeU](#cd2dsizeu__cd2dsizeu)|Overloaded. Constructs a `CD2DSizeU` object from `D2D1_SIZE_U` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DSizeU::IsNull](#cd2dsizeu__isnull)|Returns a `boolean` value that indicates whether an expression contains no valid data ( `null`).|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DSizeU::operator CSize](#cd2dsizeu__operator_csize)|Converts `CD2DSizeU` to `CSize` object.|  
  
## Inheritance Hierarchy  
 `D2D1_SIZE_U`  
  
 [CD2DSizeU](../vs140/CD2DSizeU-Class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="cd2dsizeu__cd2dsizeu"></a>  CD2DSizeU::CD2DSizeU  
 Constructs a CD2DSizeU object from CSize object.  
  
```  
CD2DSizeU(  
   const CSize& size  
);  
CD2DSizeU(  
   const D2D1_SIZE_U& size  
);  
CD2DSizeU(  
   const D2D1_SIZE_U* size  
);  
CD2DSizeU(  
   UINT32 cx = 0,  
   UINT32 cy = 0  
);  
```  
  
### Parameters  
 `size`  
 source size  
  
 `cx`  
 source width  
  
 `cy`  
 source height  
  
##  <a name="cd2dsizeu__isnull"></a>  CD2DSizeU::IsNull  
 Returns a Boolean value that indicates whether an expression contains no valid data (Null).  
  
```  
BOOL IsNull() const;  
```  
  
### Return Value  
 TRUE if width and height are empty; otherwise FALSE.  
  
##  <a name="cd2dsizeu__operator_csize"></a>  CD2DSizeU::operator CSize  
 Converts CD2DSizeU to CSize object.  
  
```  
operator CSize();  
```  
  
### Return Value  
 Current value of D2D size.  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)