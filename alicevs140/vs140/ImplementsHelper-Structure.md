---
title: "ImplementsHelper Structure"
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
ms.assetid: b857ba80-81bd-4e53-92b6-210991954243
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ImplementsHelper Structure
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   typename RuntimeClassFlagsT,  
   typename ILst,  
   bool IsDelegateToClass  
>  
friend struct Details::ImplementsHelper;  
```  
  
#### Parameters  
 `RuntimeClassFlagsT`  
 A field of flags that specifies one or more [RuntimeClassType](../vs140/RuntimeClassType-Enumeration.md) enumerators.  
  
 `ILst`  
 A list of interface IDs.  
  
 `IsDelegateToClass`  
 Specify `true` if the current instance of Implements is a base class of the first interface ID in `ILst`; otherwise, `false`.  
  
## Remarks  
 Helps implement the [Implements](../vs140/Implements-Structure.md) structure.  
  
 This template traverses a list of interfaces and adds them as base classes, and as information necessary to enable QueryInterface.  
  
## Members  
  
## Inheritance Hierarchy  
 `ImplementsHelper`  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Reference (Windows Runtime Library)](assetId:///00000000-0000-0000-0000-000000000000)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)