---
title: "CComSafeArrayBound Class"
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
ms.assetid: dd6299db-5f84-4630-bbf0-f5add5318437
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArrayBound Class
This class is a wrapper for a [SAFEARRAYBOUND](assetId:///303a9bdb-71d6-4f14-8747-84cf84936c6d) structure.  
  
## Syntax  
  
```  
  
class CComSafeArrayBound : public SAFEARRAYBOUND  
  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CComSafeArrayBound](../vs140/CComSafeArrayBound--CComSafeArrayBound.md)|The constructor.|  
|[GetCount](../vs140/CComSafeArrayBound--GetCount.md)|Call this method to return the number of elements.|  
|[GetLowerBound](../vs140/CComSafeArrayBound--GetLowerBound.md)|Call this method to return the lower bound.|  
|[GetUpperBound](../vs140/CComSafeArrayBound--GetUpperBound.md)|Call this method to return the upper bound.|  
|[SetCount](../vs140/CComSafeArrayBound--SetCount.md)|Call this method to set the number of elements.|  
|[SetLowerBound](../vs140/CComSafeArrayBound--SetLowerBound.md)|Call this method to set the lower bound.|  
  
### Operators  
  
|||  
|-|-|  
|[operator =](../vs140/CComSafeArrayBound--operator-=.md)|Sets the `CComSafeArrayBound` to a new value.|  
  
## Remarks  
 This class is a wrapper for the **SAFEARRAYBOUND** structure used by [CComSafeArray](../vs140/CComSafeArray-Class.md). It provides methods for querying and setting the upper and lower bounds of a single dimension of a `CComSafeArray` object and the number of elements it contains. A multidimensional `CComSafeArray` object uses an array of `CComSafeArrayBound` objects, one for each dimension. Therefore, when using methods such as [GetCount](../vs140/CComSafeArrayBound--GetCount.md), be aware that this method will not return the total number of elements in a multidimensional array.  
  
 **Header:** atlsafe.h  
  
## Requirements  
 **Header:** atlsafe.h  
  
##  <a name="ccomsafearraybound__ccomsafearraybound"></a>  CComSafeArrayBound::CComSafeArrayBound  
 The constructor.  
  
```  
  
CComSafeArrayBound(  
      ULONG  ulCount  
    = 0,  
      LONG  lLowerBound  
    = 0   
   ) throw( );  
  
```  
  
### Parameters  
 `ulCount`  
 The number of elements in the array.  
  
 `lLowerBound`  
 The lower bound from which the array is numbered.  
  
### Remarks  
 If the array is to be accessed from a Visual C++ program, it is recommended that the lower bound be defined as 0. It may be preferable to use a different lower bound value if the array is to be used with other languages, such as Visual Basic.  
  
##  <a name="ccomsafearraybound__getcount"></a>  CComSafeArrayBound::GetCount  
 Call this method to return the number of elements.  
  
```  
  
ULONG GetCount( ) const throw( );  
  
```  
  
### Return Value  
 Returns the number of elements.  
  
### Remarks  
 If the associated `CComSafeArray` object represents a multidimensional array, this method will only return the total number of elements in the rightmost dimension. Use [CComSafeArray::GetCount](../vs140/CComSafeArray--GetCount.md) to obtain the total number of elements.  
  
##  <a name="ccomsafearraybound__getlowerbound"></a>  CComSafeArrayBound::GetLowerBound  
 Call this method to return the lower bound.  
  
```  
  
LONG GetLowerBound( ) const throw( );  
  
```  
  
### Return Value  
 Returns the lower bound of the `CComSafeArrayBound` object.  
  
##  <a name="ccomsafearraybound__getupperbound"></a>  CComSafeArrayBound::GetUpperBound  
 Call this method to return the upper bound.  
  
```  
  
LONG GetUpperBound( ) const throw( );  
  
```  
  
### Return Value  
 Returns the upper bound of the `CComSafeArrayBound` object.  
  
### Remarks  
 The upper bound depends on the number of elements and the lower bound value. For example, if the lower bound is 0 and the number of elements is 10, the upper bound will automatically be set to 9.  
  
##  <a name="ccomsafearraybound__operator__eq"></a>  CComSafeArrayBound::operator =  
 Sets the `CComSafeArrayBound` to a new value.  
  
```  
  
CComSafeArrayBound & operator =(  
      const CComSafeArrayBound &  bound  
   ) throw( );  
   CComSafeArrayBound & operator =(  
      ULONG  ulCount  
   ) throw( );  
  
```  
  
### Parameters  
 `bound`  
 A `CComSafeArrayBound` object.  
  
 `ulCount`  
 The number of elements.  
  
### Return Value  
 Returns a pointer to the `CComSafeArrayBound` object.  
  
### Remarks  
 The `CComSafeArrayBound` object can be assigned using an existing `CComSafeArrayBound`, or by supplying the number of elements, in which case the lower bound is set to 0 by default.  
  
##  <a name="ccomsafearraybound__setcount"></a>  CComSafeArrayBound::SetCount  
 Call this method to set the number of elements.  
  
```  
  
ULONG SetCount(  
      ULONG  ulCount  
   ) throw( );  
  
```  
  
### Parameters  
 `ulCount`  
 The number of elements.  
  
### Return Value  
 Returns the number of elements in the `CComSafeArrayBound` object.  
  
##  <a name="ccomsafearraybound__setlowerbound"></a>  CComSafeArrayBound::SetLowerBound  
 Call this method to set the lower bound.  
  
```  
  
LONG SetLowerBound(  
      LONG  lLowerBound  
   ) throw( );  
  
```  
  
### Parameters  
 `lLowerBound`  
 The lower bound.  
  
### Return Value  
 Returns the new lower bound of the `CComSafeArrayBound` object.  
  
### Remarks  
 If the array is to be accessed from a Visual C++ program, it is recommended that the lower bound be defined as 0. It may be preferable to use a different lower bound value if the array is to be used with other languages, such as Visual Basic.  
  
 The upper bound depends on the number of elements and the lower bound value. For example, if the lower bound is 0 and the number of elements is 10, the upper bound will automatically be set to 9.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)