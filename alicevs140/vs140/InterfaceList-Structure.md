---
title: "InterfaceList Structure"
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
ms.assetid: 6ec3228d-eb3e-4b7e-aef1-7dcf17bdf61a
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InterfaceList Structure
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   typename T,  
   typename U  
>  
struct InterfaceList;  
```  
  
#### Parameters  
 `T`  
 An interface name; the first interface in the recursive list.  
  
 `U`  
 An interface name; the remaining interfaces in the recursive list.  
  
## Remarks  
 Used to create a recursive list of interfaces.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`FirstT`|Synonym for template parameter `T`.|  
|`RestT`|Synonym for template parameter `U`.|  
  
## Inheritance Hierarchy  
 `InterfaceList`  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)