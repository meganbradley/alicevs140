---
title: "max_fixed_size Class"
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
ms.assetid: 8c8f4588-37e9-4579-8168-ba3553800914
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# max_fixed_size Class
Describes a [max class](../vs140/-allocators-.md) object that limits a [freelist](../vs140/freelist-Class.md) object to a fixed maximum length.  
  
## Syntax  
  
```  
template <std::size_t Max> class max_fixed_size  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Max`|The max class that determines the maximum number of elements to store in the `freelist`.|  
  
### Constructors  
  
|||  
|-|-|  
|[max_fixed_size](#max_fixed_size__max_fixed_size)|Constructs an object of type `max_fixed_size`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[allocated](#max_fixed_size__allocated)|Increments the count of allocated memory blocks.|  
|[deallocated](#max_fixed_size__deallocated)|Decrements the count of allocated memory blocks.|  
|[full](#max_fixed_size__full)|Returns a value that specifies whether more memory blocks should be added to the free list.|  
|[released](#max_fixed_size__released)|Decrements the count of memory blocks on the free list.|  
|[saved](#max_fixed_size__saved)|Increments the count of memory blocks on the free list.|  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
##  <a name="max_fixed_size__allocated"></a>  max_fixed_size::allocated  
 Increments the count of allocated memory blocks.  
  
```  
void allocated(std::size_t _Nx = 1);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Nx`|The increment value.|  
  
### Remarks  
 The member function does nothing. This member function is called after each successful call by `cache_freelist::allocate` to operator `new`. The argument `_Nx` is the number of memory blocks in the chunk allocated by operator `new`.  
  
##  <a name="max_fixed_size__deallocated"></a>  max_fixed_size::deallocated  
 Decrements the count of allocated memory blocks.  
  
```  
void deallocated(std::size_t _Nx = 1);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Nx`|The increment value.|  
  
### Remarks  
 The member function does nothing. This member function is called after each call by `cache_freelist::deallocate` to operator `delete`. The argument `_Nx` is the number of memory blocks in the chunk deallocated by operator `delete`.  
  
##  <a name="max_fixed_size__full"></a>  max_fixed_size::full  
 Returns a value that specifies whether more memory blocks should be added to the free list.  
  
```  
bool full();  
```  
  
### Return Value  
 `true` if `Max <= _Nblocks`; otherwise, `false`.  
  
### Remarks  
 This member function is called by `cache_freelist::deallocate`. If the call returns `true`, `deallocate` puts the memory block on the free list; if it returns false, `deallocate` calls operator `delete` to deallocate the block.  
  
##  <a name="max_fixed_size__max_fixed_size"></a>  max_fixed_size::max_fixed_size  
 Constructs an object of type `max_fixed_size`.  
  
```  
max_fixed_size();  
```  
  
### Remarks  
 This constructor initializes the stored value `_Nblocks` to zero.  
  
##  <a name="max_fixed_size__released"></a>  max_fixed_size::released  
 Decrements the count of memory blocks on the free list.  
  
```  
void released();  
```  
  
### Remarks  
 Decrements the stored value `_Nblocks`. The `released` member function of the current [max class](../vs140/-allocators-.md) is called by `cache_freelist::allocate` whenever it removes a memory block from the free list.  
  
##  <a name="max_fixed_size__saved"></a>  max_fixed_size::saved  
 Increments the count of memory blocks on the free list.  
  
```  
void saved();  
```  
  
### Remarks  
 This member function increments the stored value `_Nblocks`. This member function is called by `cache_freelist::deallocate` whenever it puts a memory block on the free list.  
  
## See Also  
 [<allocators\>](../vs140/-allocators-.md)