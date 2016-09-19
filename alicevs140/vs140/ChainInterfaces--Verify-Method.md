---
title: "ChainInterfaces::Verify Method"
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
ms.assetid: c591e130-8686-4130-ba69-1aaedc250038
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ChainInterfaces::Verify Method
Verifies that each interface defined by template parameters `I0` through `I9` inherits from IUnknown and/or IInspectable, and that `I0` inherits from `I1` through `I9`.  
  
## Syntax  
  
```  
WRL_NOTHROW __forceinline static void Verify();  
```  
  
## Remarks  
 If the verification operation fails, a `static_assert` emits an error message describing the failure.  
  
## Remarks  
 Template parameters `I0` and `I1` are required, and parameters `I2` through `I9` are optional.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ChainInterfaces Structure](../vs140/ChainInterfaces-Structure.md)