---
title: "CAutoPtrElementTraits Class"
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
ms.assetid: 777c1b14-6ab7-491f-b9a5-be149e71d4a2
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtrElementTraits Class
This class provides methods, static functions, and typedefs useful when creating collections of smart pointers.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template<  
   typename  T>  
   class CAutoPtrElementTraits : public CDefaultElementTraits<  
   ATL::CAutoPtr<  T>>  
  
```  
  
#### Parameters  
 `T`  
 The pointer type.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CAutoPtrElementTraits::INARGTYPE](../vs140/CAutoPtrElementTraits--INARGTYPE.md)|The data type to use for adding elements to the collection class object.|  
|[CAutoPtrElementTraits::OUTARGTYPE](../vs140/CAutoPtrElementTraits--OUTARGTYPE.md)|The data type to use for retrieving elements from the collection class object.|  
  
## Remarks  
 This class provides methods, static functions, and typedefs for aiding the creation of collection class objects containing smart pointers. The classes [CAutoPtrArray](../vs140/CAutoPtrArray-Class.md) and [CAutoPtrList](../vs140/CAutoPtrList-Class.md) derive from `CAutoPtrElementTraits`. If building a collection of smart pointers that requires vector new and delete operators, use [CAutoVectorPtrElementTraits](../vs140/CAutoVectorPtrElementTraits-Class.md) instead.  
  
## Inheritance Hierarchy  
 [CDefaultCompareTraits](../vs140/CDefaultCompareTraits-Class.md)  
  
 [CDefaultHashTraits](../vs140/CDefaultHashTraits-Class.md)  
  
 [CElementTraitsBase](../vs140/CElementTraitsBase-Class.md)  
  
 [CDefaultElementTraits](../vs140/CDefaultElementTraits-Class.md)  
  
 `CAutoPtrElementTraits`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="cautoptrelementtraits__inargtype"></a>  CAutoPtrElementTraits::INARGTYPE  
 The data type to use for adding elements to the collection class object.  
  
```  
  
typedef CAutoPtr<T> & INARGTYPE;  
  
```  
  
##  <a name="cautoptrelementtraits__outargtype"></a>  CAutoPtrElementTraits::OUTARGTYPE  
 The data type to use for retrieving elements from the collection class object.  
  
```  
  
typedef T *& OUTARGTYPE;  
  
```  
  
## See Also  
 [CDefaultElementTraits Class](../vs140/CDefaultElementTraits-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)