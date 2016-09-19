---
title: "allocator_base::construct"
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
ms.assetid: bd13f467-35cd-4031-8359-79645c4ebdf3
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# allocator_base::construct
Constructs a specific type of object at a specified address that is initialized with a specified value.  
  
## Syntax  
  
```  
void construct(pointer _Ptr, const Type& _Val);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Ptr`|A pointer to the location where the object is to be constructed.|  
|`_Val`|The value with which the object being constructed is to be initialized.|  
  
## Remarks  
 This member function is implemented for the user-defined allocator by calling `new((void*)_Ptr Type(_Val)`.  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [allocator_base Class](../vs140/allocator_base-Class.md)