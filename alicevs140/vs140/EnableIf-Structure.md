---
title: "EnableIf Structure"
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
ms.assetid: 7825b283-e6b2-4f39-a4b9-c03bcd431b8e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EnableIf Structure
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   bool b,  
   typename T = void  
>  
  
struct EnableIf;  
template <  
   typename T  
>  
struct EnableIf<true, T>;  
```  
  
#### Parameters  
 `T`  
 A type.  
  
 `b`  
 A Boolean expression.  
  
## Remarks  
 Defines a data member of the type specified by the second template parameter if the first template parameter evaluates to `true`.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`type`|If template parameter `b` evaluates to `true`, the partial specialization defines data member `type` to be of type `T`.|  
  
## Inheritance Hierarchy  
 `EnableIf`  
  
## Requirements  
 **Header:** internal.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)