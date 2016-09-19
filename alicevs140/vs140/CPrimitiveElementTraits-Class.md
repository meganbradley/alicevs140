---
title: "CPrimitiveElementTraits Class"
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
ms.assetid: 21c1cea8-2c5a-486c-b65c-85490f3ed4e6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrimitiveElementTraits Class
This class provides default methods and functions for a collection class composed of primitive data types.  
  
## Syntax  
  
```  
  
template<  
      typename  T  
   > class CPrimitiveElementTraits :   
      public CDefaultElementTraits<  T  
    >  
  
```  
  
#### Parameters  
 `T`  
 The type of data to be stored in the collection class object.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CPrimitiveElementTraits::INARGTYPE](../vs140/CPrimitiveElementTraits--INARGTYPE.md)|The data type to use for adding elements to the collection class object.|  
|[CPrimitiveElementTraits::OUTARGTYPE](../vs140/CPrimitiveElementTraits--OUTARGTYPE.md)|The data type to use for retrieving elements from the collection class object.|  
  
## Remarks  
 This class provides default static functions and methods for moving, copying, comparing, and hashing primitive data type elements stored in a collection class object.  
  
 For more information, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Inheritance Hierarchy  
 [CDefaultCompareTraits](../vs140/CDefaultCompareTraits-Class.md)  
  
 [CDefaultHashTraits](../vs140/CDefaultHashTraits-Class.md)  
  
 [CElementTraitsBase](../vs140/CElementTraitsBase-Class.md)  
  
 [CDefaultElementTraits](../vs140/CDefaultElementTraits-Class.md)  
  
 `CPrimitiveElementTraits`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="cprimitiveelementtraits__inargtype"></a>  CPrimitiveElementTraits::INARGTYPE  
 The data type to use for adding elements to the collection class object.  
  
```  
  
typedef T INARGTYPE;  
  
```  
  
##  <a name="cprimitiveelementtraits__outargtype"></a>  CPrimitiveElementTraits::OUTARGTYPE  
 The data type to use for retrieving elements from the collection class object.  
  
```  
  
typedef T & OUTARGTYPE;  
  
```  
  
## See Also  
 [CDefaultElementTraits Class](../vs140/CDefaultElementTraits-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)