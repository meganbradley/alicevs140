---
title: "ChainInterfaces::CastToUnknown Method"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: a6a58555-e5b0-4773-aba0-959d9d362c6b
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ChainInterfaces::CastToUnknown Method
Casts the interface pointer of the type defined by the `I0` template parameter to a pointer to IUnknown.  
  
## Syntax  
  
```  
__forceinline IUnknown* CastToUnknown();  
```  
  
## Return Value  
 A pointer to IUnknown.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ChainInterfaces Structure](../vs140/ChainInterfaces-Structure.md)