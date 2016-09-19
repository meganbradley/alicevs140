---
title: "allocator_base::address"
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
ms.assetid: a49503ff-b61a-4c6c-8c8b-4a1660ec2fd5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator_base::address
Finds the address of an object whose value is specified.  
  
## Syntax  
  
```  
pointer address(reference _Val);  
const_pointer address(const_reference _Val);  
```  
  
#### Parameters  
 `_Val`  
 The const or nonconst value of the object whose address is being searched for.  
  
## Return Value  
 A const or nonconst pointer to the object found of, respectively, const or nonconst value.  
  
## Remarks  
 This member function is implemented for the user-defined allocator by returning `&_Val`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [allocator_base](../vs140/allocator_base-Class.md)