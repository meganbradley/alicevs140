---
title: "MixIn Structure"
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
ms.assetid: 47e2df9b-3a2e-4ae8-8ba3-b1fd3aa73566
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MixIn Structure
Ensures that a runtime class derives from [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] interfaces, if any, and then classic COM interfaces.  
  
## Syntax  
  
```  
template<  
   typename Derived,  
   typename MixInType,  
   bool hasImplements = __is_base_of(Details::ImplementsBase,  
   MixInType)  
>  
struct MixIn;  
```  
  
#### Parameters  
 `Derived`  
 A type derived from the [Implements](../vs140/Implements-Structure.md) structure.  
  
 `MixInType`  
 A base type.  
  
 `hasImplements`  
 `true` if `MixInType` is derived from the current implementation the base type; `false` otherwise.  
  
## Remarks  
 If a class is derived from both [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] and class COM interfaces, the class declaration list must first list any [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] interfaces and then any classic COM interfaces. MixIn ensures that the interfaces are specified in the correct order.  
  
## Inheritance Hierarchy  
 `MixIn`  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)