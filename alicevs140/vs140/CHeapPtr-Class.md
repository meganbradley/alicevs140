---
title: "CHeapPtr Class"
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
ms.assetid: e5c5bfd4-9bf1-4164-8a83-8155fe253454
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtr Class
A smart pointer class for managing heap pointers.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template<  
typename   
T  
,  
class   
Allocator  
= CCRTAllocator  
> class CHeapPtr :  
public CHeapPtrBase<   
T  
,   
Allocator  
>  
  
```  
  
#### Parameters  
 `T`  
 The object type to be stored on the heap.  
  
 `Allocator`  
 The memory allocation class to use.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CHeapPtr::CHeapPtr](../vs140/CHeapPtr--CHeapPtr.md)|The constructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CHeapPtr::Allocate](../vs140/CHeapPtr--Allocate.md)|Call this method to allocate memory on the heap to store objects.|  
|[CHeapPtr::Reallocate](../vs140/CHeapPtr--Reallocate.md)|Call this method to reallocate the memory on the heap.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CHeapPtr::operator =](../vs140/CHeapPtr--operator-=.md)|The assignment operator.|  
  
## Remarks  
 `CHeapPtr` is derived from                 [CHeapPtrBase](../vs140/CHeapPtrBase-Class.md) and by default uses the CRT routines (in                 [CCRTAllocator](../vs140/CCRTAllocator-Class.md)) to allocate and free memory. The class                 [CHeapPtrList](../vs140/CHeapPtrList-Class.md) may be used to construct a list of heap pointers. See also                 [CComHeapPtr](../vs140/CComHeapPtr-Class.md), which uses COM memory allocation routines.  
  
## Inheritance Hierarchy  
 [CHeapPtrBase](../vs140/CHeapPtrBase-Class.md)  
  
 `CHeapPtr`  
  
## Requirements  
 **Header:** atlcore.h  
  
##  <a name="cheapptr__allocate"></a>  CHeapPtr::Allocate  
 Call this method to allocate memory on the heap to store objects.  
  
```  
  
bool Allocate(  
   size_t   
nElements  
 = 1   
) throw( );  
  
```  
  
### Parameters  
 `nElements`  
 The number of elements used to calculate the amount of memory to allocate. The default value is 1.  
  
### Return Value  
 Returns true if the memory was successfully allocated, false on failure.  
  
### Remarks  
 The allocator routines are used to reserve enough memory on the heap to store                         *nElement* objects of a type defined in the constructor.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#77](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#77)]  
  
##  <a name="cheapptr__cheapptr"></a>  CHeapPtr::CHeapPtr  
 The constructor.  
  
```  
  
CHeapPtr( ) throw( );   
explicit CHeapPtr(  
   T*   
p  
) throw( );  
CHeapPtr(  
   CHeapPtr< T, Allocator >&   
p  
) throw( );  
  
```  
  
### Parameters  
 `p`  
 An existing heap pointer or                                 `CHeapPtr`.  
  
### Remarks  
 The heap pointer can optionally be created using an existing pointer, or a                         `CHeapPtr` object. If so, the new                         `CHeapPtr` object assumes responsibility for managing the new pointer and resources.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#78](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#78)]  
  
##  <a name="cheapptr__operator__eq"></a>  CHeapPtr::operator =  
 Assignment operator.  
  
```  
  
CHeapPtr< T, Allocator >& operator =(  
   CHeapPtr< T, Allocator >&   
p  
) throw( );  
  
```  
  
### Parameters  
 `p`  
 An existing                                 `CHeapPtr` object.  
  
### Return Value  
 Returns a reference to the updated                         `CHeapPtr`.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#80](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#80)]  
  
##  <a name="cheapptr__reallocate"></a>  CHeapPtr::Reallocate  
 Call this method to reallocate the memory on the heap.  
  
```  
  
bool Reallocate(  
   size_t   
nElements  
) throw( );  
  
```  
  
### Parameters  
 `nElements`  
 The new number of elements used to calculate the amount of memory to allocate.  
  
### Return Value  
 Returns true if the memory was successfully allocated, false on failure.  
  
### Example  
 [!CODE [NVC_ATL_Utilities#79](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#79)]  
  
## See Also  
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)   
 [CCRTAllocator Class](../vs140/CCRTAllocator-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)