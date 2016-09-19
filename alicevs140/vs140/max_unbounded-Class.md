---
title: "max_unbounded Class"
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
ms.assetid: e34627a9-c231-4031-a483-cbb0514fff46
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# max_unbounded Class
Describes a [max class](../vs140/-allocators-.md) object that does not limit the maximum length of a [freelist](../vs140/freelist-Class.md) object.  
  
## Syntax  
  
```  
class max_unbounded  
```  
  
### Member Functions  
  
|||  
|-|-|  
|[allocated](#max_unbounded__allocated)|Increments the count of allocated memory blocks.|  
|[deallocated](#max_unbounded__deallocated)|Decrements the count of allocated memory blocks.|  
|[full](#max_unbounded__full)|Returns a value that specifies whether more memory blocks should be added to the free list.|  
|[released](#max_unbounded__released)|Decrements the count of memory blocks on the free list.|  
|[saved](#max_unbounded__saved)|Increments the count of memory blocks on the free list.|  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
##  <a name="max_unbounded__allocated"></a>  max_unbounded::allocated  
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
  
##  <a name="max_unbounded__deallocated"></a>  max_unbounded::deallocated  
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
  
##  <a name="max_unbounded__full"></a>  max_unbounded::full  
 Returns a value that specifies whether more memory blocks should be added to the free list.  
  
```  
bool full();  
```  
  
### Return Value  
 The member function always returns `false`.  
  
### Remarks  
 This member function is called by `cache_freelist::deallocate`. If the call returns `true`, `deallocate` puts the memory block on the free list; if it returns false, `deallocate` calls operator `delete` to deallocate the block.  
  
##  <a name="max_unbounded__released"></a>  max_unbounded::released  
 Decrements the count of memory blocks on the free list.  
  
```  
void released();  
```  
  
### Remarks  
 This member function does nothing. The `released` member function of the current max class is called by `cache_freelist::allocate` whenever it removes a memory block from the free list.  
  
##  <a name="max_unbounded__saved"></a>  max_unbounded::saved  
 Increments the count of memory blocks on the free list.  
  
```  
void saved();  
```  
  
### Remarks  
 This member function does nothing. It is called by `cache_freelist::deallocate` whenever it puts a memory block on the free list.  
  
## See Also  
 [<allocators\>](../vs140/-allocators-.md)