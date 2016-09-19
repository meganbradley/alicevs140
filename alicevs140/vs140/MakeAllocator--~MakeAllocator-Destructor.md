---
title: "MakeAllocator::~MakeAllocator Destructor"
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
ms.assetid: f1299c5f-cc6b-4d4e-85d4-aee1be0e2b0a
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MakeAllocator::~MakeAllocator Destructor
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
~MakeAllocator();  
```  
  
## Remarks  
 Deinitializes the current instance of the MakeAllocator class.  
  
 This destructor also deletes the underlying allocated memory if necessary.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [MakeAllocator Class](../vs140/MakeAllocator-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)