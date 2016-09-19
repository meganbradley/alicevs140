---
title: "freelist Class"
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
ms.assetid: 8ad7e35c-4c80-4479-8ede-1a2497b06d71
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# freelist Class
Manages a list of memory blocks.  
  
## Syntax  
  
```  
template <std::size_t Sz, class Max> class freelist  
    : public Max  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Sz`|The number of elements in the array to be allocated.|  
|`Max`|The max class representing the maximum number of elements to be stored in the free list. The max class can be [max_none](../vs140/max_none-Class.md), [max_unbounded](../vs140/max_unbounded-Class.md), [max_fixed_size](../vs140/max_fixed_size-Class.md), or [max_variable_size](../vs140/max_variable_size-Class.md).|  
  
## Remarks  
 This template class manages a list of memory blocks of size `Sz` with the maximum length of the list determined by the max class passed in `Max`.  
  
### Constructors  
  
|||  
|-|-|  
|[freelist](#freelist__freelist)|Constructs an object of type `freelist`.|  
  
### Member Functions  
  
|||  
|-|-|  
|[pop](#freelist__pop)|Removes the first memory block from the free list.|  
|[push](#freelist__push)|Adds a memory block to the list.|  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
##  <a name="freelist__freelist"></a>  freelist::freelist  
 Constructs an object of type `freelist`.  
  
```  
freelist();  
```  
  
### Remarks  
  
##  <a name="freelist__pop"></a>  freelist::pop  
 Removes the first memory block from the free list.  
  
```  
void *pop();  
```  
  
### Return Value  
 Returns a pointer to the memory block removed from the list.  
  
### Remarks  
 The member function returns `NULL` if the list is empty. Otherwise, it removes the first memory block from the list.  
  
##  <a name="freelist__push"></a>  freelist::push  
 Adds a memory block to the list.  
  
```  
bool push(void* _Ptr);  
```  
  
### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Ptr`|A pointer to the memory block to be added to the free list.|  
  
### Return Value  
 `true` if the `full` function of the max class returns `false`; otherwise, the `push` function returns `false`.  
  
### Remarks  
 If the `full` function of the max class returns `false`, this member function adds the memory block pointed to by `_Ptr` to the head of the list.  
  
## See Also  
 [<allocators\>](../vs140/-allocators-.md)