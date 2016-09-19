---
title: "CComHeapPtr Class"
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
ms.assetid: bd08b53d-da2b-43ab-a79c-e7c8dbbc5994
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComHeapPtr Class
A smart pointer class for managing heap pointers.  
  
## Syntax  
  
```  
  
template<  
      typename  T  
   > class CComHeapPtr :  
      public CHeapPtr<  T  
   , CComAllocator >  
  
```  
  
#### Parameters  
 `T`  
 The object type to be stored on the heap.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComHeapPtr::CComHeapPtr](../vs140/CComHeapPtr--CComHeapPtr.md)|The constructor.|  
  
## Remarks  
 `CComHeapPtr` derives from `CHeapPtr`, but uses [CComAllocator](../vs140/CComAllocator-Class.md) to allocate memory using COM routines. See [CHeapPtr](../vs140/CHeapPtr-Class.md) and [CHeapPtrBase](../vs140/CHeapPtrBase-Class.md) for the methods available.  
  
## Inheritance Hierarchy  
 [CHeapPtrBase](../vs140/CHeapPtrBase-Class.md)  
  
 [CHeapPtr](../vs140/CHeapPtr-Class.md)  
  
 `CComHeapPtr`  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="ccomheapptr__ccomheapptr"></a>  CComHeapPtr::CComHeapPtr  
 The constructor.  
  
```  
  
CComHeapPtr( ) throw( );   
   explicit CComHeapPtr(  
      T*  pData  
   ) throw( );  
  
```  
  
### Parameters  
 `pData`  
 An existing `CComHeapPtr` object.  
  
### Remarks  
 The heap pointer can optionally be created using an existing `CComHeapPtr` object. If so, the new `CComHeapPtr` object assumes responsibility for managing the new pointer and resources.  
  
## See Also  
 [CHeapPtr Class](../vs140/CHeapPtr-Class.md)   
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)   
 [CComAllocator Class](../vs140/CComAllocator-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)