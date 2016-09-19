---
title: "VerifyInheritanceHelper Structure"
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
ms.assetid: 8a48a702-0f71-4807-935b-8311f0a7a8b6
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VerifyInheritanceHelper Structure
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   typename I,  
   typename Base  
>  
struct VerifyInheritanceHelper;  
template <  
   typename I  
>  
struct VerifyInheritanceHelper<I, Nil>;  
```  
  
#### Parameters  
 `I`  
 A type.  
  
 `Base`  
 Another type.  
  
## Remarks  
 Tests whether one interface is derived from another interface.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[VerifyInheritanceHelper::Verify Method](../vs140/VerifyInheritanceHelper--Verify-Method.md)|Tests the two interfaces specified by the current template parameters and determines whether one interface is derived from the other.|  
  
## Inheritance Hierarchy  
 `VerifyInheritanceHelper`  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)