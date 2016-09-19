---
title: "max_none Class"
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
ms.assetid: 12ab5376-412e-479c-86dc-2c3d6a3559b6
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# max_none Class
Describes a [max class](../vs140/-allocators-.md) object that limits a [freelist](../vs140/freelist-Class.md) object to a maximum length of zero.  
  
## Syntax  
  
```  
template <std::size_t Max> class max_none  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Max`|The max class that determines the maximum number of elements to store in the `freelist`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[allocated](#max_none__allocated)|Increments the count of allocated memory blocks.|  
|[deallocated](#max_none__deallocated)|Decrements the count of allocated memory blocks.|  
|[full](#max_none__full)|Returns a value that specifies whether more memory blocks should be added to the free list.|  
|[released](#max_none__released)|Decrements the count of memory blocks on the free list.|  
|[saved](#max_none__saved)|Increments the count of memory blocks on the free list.|  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
##  <a name="max_none__allocated"></a>  max_none::allocated  
 Increments the count of allocated memory blocks.  
  
```  
void allocated(std::size_t _Nx = 1);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Nx`|The increment value.|  
  
### Remarks  
 This member function does nothing. It is called after each successful call by `cache_freelist::allocate` to operator `new`. The argument `_Nx` is the number of memory blocks in the chunk allocated by operator `new`.  
  
##  <a name="max_none__deallocated"></a>  max_none::deallocated  
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
  
##  <a name="max_none__full"></a>  max_none::full  
 Returns a value that specifies whether more memory blocks should be added to the free list.  
  
```  
bool full();  
```  
  
### Return Value  
 This member function always returns `true`.  
  
### Remarks  
 This member function is called by `cache_freelist::deallocate`. If the call returns `true`, `deallocate` puts the memory block on the free list; if it returns false, `deallocate` calls operator `delete` to deallocate the block.  
  
##  <a name="max_none__released"></a>  max_none::released  
 Decrements the count of memory blocks on the free list.  
  
```  
void released();  
```  
  
### Remarks  
 This member function does nothing. The `released` member function of the current max class is called by `cache_freelist::allocate` whenever it removes a memory block from the free list.  
  
##  <a name="max_none__saved"></a>  max_none::saved  
 Increments the count of memory blocks on the free list.  
  
```  
void saved();  
```  
  
### Remarks  
 This member function does nothing. It is called by `cache_freelist::deallocate` whenever it puts a memory block on the free list.  
  
## See Also  
 [<allocators\>](../vs140/-allocators-.md)