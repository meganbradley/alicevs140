---
title: "CComQIPtrElementTraits Class"
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
ms.assetid: 9df9250a-5413-4362-b133-332932a597c4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComQIPtrElementTraits Class
This class provides methods, static functions, and typedefs useful when creating collections of COM interface pointers.  
  
## Syntax  
  
```  
  
template<  
      typename  I,  
      const IID*  piid  
    = & __uuidof(  I  
    )   
   >   
   class CComQIPtrElementTraits : public CDefaultElementTraits<  
      ATL::CComQIPtr<  I  
   ,  piid  
    >>  
  
```  
  
#### Parameters  
 `I`  
 A COM interface specifying the type of pointer to be stored.  
  
 `piid`  
 A pointer to the IID of `I`.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CComQIPtrElementTraits::INARGTYPE](../vs140/CComQIPtrElementTraits--INARGTYPE.md)|The data type to use for adding elements to the collection class object.|  
  
## Remarks  
 This class derives methods and provides a typedef useful when creating a collection class of [CComQIPtr](../vs140/CComQIPtr-Class.md) COM interface pointer objects. This class is utilized by both the [CInterfaceArray](../vs140/CInterfaceArray-Class.md) and [CInterfaceList](../vs140/CInterfaceList-Class.md) classes.  
  
 For more information, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Inheritance Hierarchy  
 [CDefaultCompareTraits](../vs140/CDefaultCompareTraits-Class.md)  
  
 [CDefaultHashTraits](../vs140/CDefaultHashTraits-Class.md)  
  
 [CElementTraitsBase](../vs140/CElementTraitsBase-Class.md)  
  
 [CDefaultElementTraits](../vs140/CDefaultElementTraits-Class.md)  
  
 `CComQIPtrElementTraits`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="ccomqiptrelementtraits__inargtype"></a>  CComQIPtrElementTraits::INARGTYPE  
 The data type to use for adding elements to the collection class object.  
  
```  
  
typedef I * INARGTYPE;  
  
```  
  
## See Also  
 [CDefaultElementTraits Class](../vs140/CDefaultElementTraits-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)