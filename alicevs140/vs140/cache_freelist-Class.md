---
title: "cache_freelist Class"
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
ms.topic: article
ms.assetid: 840694de-36ba-470f-8dae-2b723d5a8cd9
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# cache_freelist Class
Defines a [block allocator](../vs140/-allocators-.md) that allocates and deallocates memory blocks of a single size.  
  
## Syntax  
  
```  
template <std::size_t Sz, class Max> class cache_freelist  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Sz`|The number of elements in the array to be allocated.|  
|`Max`|The max class representing the maximum size of the free list. This can be [max_fixed_size](../vs140/max_fixed_size-Class.md), [max_none](../vs140/max_none-Class.md), [max_unbounded](../vs140/max_unbounded-Class.md), or [max_variable_size](../vs140/max_variable_size-Class.md).|  
  
## Remarks  
 The cache_freelist template class maintains a free list of memory blocks of size `Sz`. When the free list is full it uses `operator delete` to deallocate memory blocks. When the free list is empty it uses `operator new` to allocate new memory blocks. The maximum size of the free list is determined by the class max class passed in the `Max` parameter.  
  
 Each memory block holds `Sz` bytes of usable memory and the data that `operator new` and `operator delete` require.  
  
### Constructors  
  
|||  
|-|-|  
|[cache_freelist](#cache_freelist__cache_freelist)|Constructs an object of type `cache_freelist`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[allocate](#cache_freelist__allocate)|Allocates a block of memory.|  
|[deallocate](#cache_freelist__deallocate)|Frees a specified number of objects from storage beginning at a specified position.|  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
##  <a name="cache_freelist__allocate"></a>  cache_freelist::allocate  
 Allocates a block of memory.  
  
```  
void *allocate(std::size_t _Count);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Count`|The number of elements in the array to be allocated.|  
  
### Return Value  
 A pointer to the allocated object.  
  
### Remarks  
  
##  <a name="cache_freelist__cache_freelist"></a>  cache_freelist::cache_freelist  
 Constructs an object of type `cache_freelist`.  
  
```  
cache_freelist();  
```  
  
### Remarks  
  
##  <a name="cache_freelist__deallocate"></a>  cache_freelist::deallocate  
 Frees a specified number of objects from storage beginning at a specified position.  
  
```  
void deallocate(void* _Ptr, std::size_t _Count);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Ptr`|A pointer to the first object to be deallocated from storage.|  
|`_Count`|The number of objects to be deallocated from storage.|  
  
### Remarks  
  
## See Also  
 [<allocators\>](../vs140/-allocators-.md)