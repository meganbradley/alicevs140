---
title: "allocator::deallocate"
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
ms.assetid: 8228bf56-a124-466a-86a6-567e7f46a778
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator::deallocate
Frees a specified number of objects from storage beginning at a specified position.  
  
## Syntax  
  
```  
  
      void deallocate(  
   pointer _Ptr,   
   size_type _Count  
);  
```  
  
#### Parameters  
 `_Ptr`  
 A pointer to the first object to be deallocated from storage.  
  
 `_Count`  
 The number of objects to be deallocated from storage.  
  
## Remarks  
 The member function frees storage for the array of count objects of type **Type** beginning at `_Ptr`, by calling `operator delete`(`_Ptr`). The pointer `_Ptr` must have been returned earlier by a call to [allocate](../vs140/allocator--allocate.md) for an allocator object that compares equal to **\*this**, allocating an array object of the same size and type. `deallocate` never throws an exception.  
  
## Example  
 For an example using the member function, see [allocator::allocate](../vs140/allocator--allocate.md).  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [allocator Class](../vs140/allocator-Class.md)