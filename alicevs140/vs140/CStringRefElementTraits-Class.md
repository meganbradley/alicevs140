---
title: "CStringRefElementTraits Class"
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
ms.assetid: cc15062d-5627-46cc-ac2b-1744afdc2dbd
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringRefElementTraits Class
This class provides static functions related to strings stored in collection class objects. The string objects are dealt with as references.  
  
## Syntax  
  
```  
  
template<   
      typename  T>  
   class CStringRefElementTraits : public CElementTraitsBase<  T  
    >  
  
```  
  
#### Parameters  
 `T`  
 The type of data to be stored in the collection.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CStringRefElementTraits::CompareElements](../vs140/CStringRefElementTraits--CompareElements.md)|Call this static function to compare two string elements for equality.|  
|[CStringRefElementTraits::CompareElementsOrdered](../vs140/CStringRefElementTraits--CompareElementsOrdered.md)|Call this static function to compare two string elements.|  
|[CStringRefElementTraits::Hash](../vs140/CStringRefElementTraits--Hash.md)|Call this static function to calculate a hash value for the given string element.|  
  
## Remarks  
 This class provides static functions for comparing strings and for creating a hash value. These functions are useful when using a collection class to store string-based data. Unlike [CStringElementTraits](../vs140/CStringElementTraits-Class.md) and [CStringElementTraitsI](../vs140/CStringElementTraitsI-Class.md), `CStringRefElementTraits` causes the `CString` arguments to be passed as **const CString&** references.  
  
 For more information, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Inheritance Hierarchy  
 [CElementTraitsBase](../vs140/CElementTraitsBase-Class.md)  
  
 `CStringRefElementTraits`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="cstringrefelementtraits__compareelements"></a>  CStringRefElementTraits::CompareElements  
 Call this static function to compare two string elements for equality.  
  
```  
  
static bool CompareElements(  
      INARGTYPE  element1,  
      INARGTYPE  element2  
   ) throw( );  
  
```  
  
### Parameters  
 `element1`  
 The first string element.  
  
 `element2`  
 The second string element.  
  
### Return Value  
 Returns true if the elements are equal, false otherwise.  
  
##  <a name="cstringrefelementtraits__compareelementsordered"></a>  CStringRefElementTraits::CompareElementsOrdered  
 Call this static function to compare two string elements.  
  
```  
  
static int CompareElementsOrdered(  
      INARGTYPE  str1,  
      INARGTYPE  str2  
   ) throw( );  
  
```  
  
### Parameters  
 `str1`  
 The first string element.  
  
 `str2`  
 The second string element.  
  
### Return Value  
 Zero if the strings are identical, < 0 if `str1` is less than `str2`, or > 0 if `str1` is greater than `str2`. The [CStringT::Compare](../vs140/CStringT--Compare.md) method is used to perform the comparisons.  
  
##  <a name="cstringrefelementtraits__hash"></a>  CStringRefElementTraits::Hash  
 Call this static function to calculate a hash value for the given string element.  
  
```  
  
static ULONG Hash(  
      INARGTYPE  str  
   ) throw( );  
  
```  
  
### Parameters  
 `str`  
 The string element.  
  
### Return Value  
 Returns a hash value, calculated using the string's contents.  
  
## See Also  
 [CElementTraitsBase Class](../vs140/CElementTraitsBase-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)