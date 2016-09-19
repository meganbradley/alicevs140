---
title: "CHeapPtrElementTraits Class"
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
ms.assetid: 910e0e06-3c8b-4242-bf00-b57eb74fbc77
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrElementTraits Class
This class provides methods, static functions, and typedefs useful when creating collections of heap pointers.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template<  
   typename  T,  
   class  Allocator  
   = ATL::CCRTAllocator>  
   class CHeapPtrElementTraits : public CDefaultElementTraits<  
   ATL::CHeapPtr<  T  
   ,  Allocator>>  
  
```  
  
#### Parameters  
 `T`  
 The object type to be stored in the collection class.  
  
 `Allocator`  
 The memory allocation class to use. The default is [CCRTAllocator](../vs140/CCRTAllocator-Class.md).  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CHeapPtrElementTraits::INARGTYPE](../vs140/CHeapPtrElementTraits--INARGTYPE.md)|The data type to use for adding elements to the collection class object.|  
|[CHeapPtrElementTraits::OUTARGTYPE](../vs140/CHeapPtrElementTraits--OUTARGTYPE.md)|The data type to use for retrieving elements from the collection class object.|  
  
## Remarks  
 This class provides methods, static functions, and typedefs for aiding the creation of collection class objects containing heap pointers. The class `CHeapPtrList` derives from `CHeapPtrElementTraits`.  
  
 For more information, see [ATL Collection Classes](../vs140/ATL-Collection-Classes.md).  
  
## Inheritance Hierarchy  
 [CDefaultCompareTraits](../vs140/CDefaultCompareTraits-Class.md)  
  
 [CDefaultHashTraits](../vs140/CDefaultHashTraits-Class.md)  
  
 [CElementTraitsBase](../vs140/CElementTraitsBase-Class.md)  
  
 [CDefaultElementTraits](../vs140/CDefaultElementTraits-Class.md)  
  
 `CHeapPtrElementTraits`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="cheapptrelementtraits__inargtype"></a>  CHeapPtrElementTraits::INARGTYPE  
 The data type to use for adding elements to the collection class object.  
  
```  
  
typedef CHeapPtr<T,  
   Allocator> & INARGTYPE;  
  
```  
  
##  <a name="cheapptrelementtraits__outargtype"></a>  CHeapPtrElementTraits::OUTARGTYPE  
 The data type to use for retrieving elements from the collection class object.  
  
```  
  
typedef T *& OUTARGTYPE;  
  
```  
  
## See Also  
 [CDefaultElementTraits Class](../vs140/CDefaultElementTraits-Class.md)   
 [CComHeapPtr Class](../vs140/CComHeapPtr-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)