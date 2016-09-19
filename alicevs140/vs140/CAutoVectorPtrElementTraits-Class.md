---
title: "CAutoVectorPtrElementTraits Class"
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
ms.assetid: 16b81a56-55fb-46ca-b376-66a1884231a6
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoVectorPtrElementTraits Class
This class provides methods, static functions, and typedefs useful when creating collections of smart pointers using vector new and delete operators.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template<  
   typename  T>  
   class CAutoVectorPtrElementTraits : public CDefaultElementTraits<  
   ATL::CAutoVectorPtr<  T>>  
  
```  
  
#### Parameters  
 `T`  
 The pointer type.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CAutoVectorPtrElementTraits::INARGTYPE](../vs140/CAutoVectorPtrElementTraits--INARGTYPE.md)|The data type to use for adding elements to the collection class object.|  
|[CAutoVectorPtrElementTraits::OUTARGTYPE](../vs140/CAutoVectorPtrElementTraits--OUTARGTYPE.md)|The data type to use for retrieving elements from the collection class object.|  
  
## Remarks  
 This class provides methods, static functions, and typedefs for aiding the creation of collection class objects containing smart pointers. Unlike [CAutoPtrElementTraits](../vs140/CAutoPtrElementTraits-Class.md), this class uses vector new and delete operators.  
  
## Inheritance Hierarchy  
 [CDefaultCompareTraits](../vs140/CDefaultCompareTraits-Class.md)  
  
 [CDefaultHashTraits](../vs140/CDefaultHashTraits-Class.md)  
  
 [CElementTraitsBase](../vs140/CElementTraitsBase-Class.md)  
  
 [CDefaultElementTraits](../vs140/CDefaultElementTraits-Class.md)  
  
 `CAutoVectorPtrElementTraits`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="cautovectorptrelementtraits__inargtype"></a>  CAutoVectorPtrElementTraits::INARGTYPE  
 The data type to use for adding elements to the collection class object.  
  
```  
  
typedef CAutoVectorPtr<T> & INARGTYPE;  
  
```  
  
##  <a name="cautovectorptrelementtraits__outargtype"></a>  CAutoVectorPtrElementTraits::OUTARGTYPE  
 The data type to use for retrieving elements from the collection class object.  
  
```  
  
typedef T *& OUTARGTYPE;  
  
```  
  
## See Also  
 [CDefaultElementTraits Class](../vs140/CDefaultElementTraits-Class.md)   
 [CAutoVectorPtr Class](../vs140/CAutoVectorPtr-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)