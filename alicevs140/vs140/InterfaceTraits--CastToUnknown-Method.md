---
title: "InterfaceTraits::CastToUnknown Method"
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
ms.assetid: aca47fa0-3c60-47f2-a73c-258f7160adff
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InterfaceTraits::CastToUnknown Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template<  
   typename T  
>  
static __forceinline IUnknown* CastToUnknown(  
   _In_ T* ptr  
);  
```  
  
#### Parameters  
 `T`  
 The type of parameter `ptr`.  
  
 `ptr`  
 Pointer to type `T`.  
  
## Return Value  
 Pointer to the IUnknown from which `Base` is derived.  
  
## Remarks  
 Casts the specified pointer to a pointer to IUnknown.  
  
 For more information about `Base`, see the Public Typedefs section in [InterfaceTraits Structure](../vs140/InterfaceTraits-Structure.md).  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [InterfaceTraits Structure](../vs140/InterfaceTraits-Structure.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)