---
title: "MakeAllocator::Allocate Method"
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
ms.assetid: a01997bc-4ff1-4ed0-9def-e4aaa15b0598
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MakeAllocator::Allocate Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
__forceinline void* Allocate();  
```  
  
## Return Value  
 If successful, a pointer to the allocated memory; otherwise, `nullptr`.  
  
## Remarks  
 Allocates memory and associates it with the current MakeAllocator object.  
  
 The size of the allocated memory is the size of the type specified by the current MakeAllocator template parameter.  
  
 A developer needs to override only the Allocate() method to implement a different memory allocation model.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [MakeAllocator Class](../vs140/MakeAllocator-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)