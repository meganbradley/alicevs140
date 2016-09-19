---
title: "MakeAllocator::Detach Method"
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
ms.assetid: 78012634-2dda-4ea2-9ffe-40f105d2fe47
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MakeAllocator::Detach Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
__forceinline void Detach();  
```  
  
## Remarks  
 Disassociates memory allocated by the [Allocate](../vs140/MakeAllocator--Allocate-Method.md) method from the current MakeAllocator object.  
  
 If you call Detach(), you are responsible for deleting the memory provided by the Allocate method.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [MakeAllocator Class](../vs140/MakeAllocator-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)