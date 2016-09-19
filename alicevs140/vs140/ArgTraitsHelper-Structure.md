---
title: "ArgTraitsHelper Structure"
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
ms.assetid: e3f798da-0aef-4a57-95d3-d38c34c47d72
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ArgTraitsHelper Structure
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template<  
   typename TDelegateInterface  
>  
struct ArgTraitsHelper;  
```  
  
#### Parameters  
 `TDelegateInterface`  
 A delegate interface.  
  
## Remarks  
 Helps define common characteristics of delegate arguments.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`methodType`|A synonym for `decltype(&TDelegateInterface::Invoke)`.|  
|`Traits`|A synonym for `ArgTraits<methodType>`.|  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|[ArgTraitsHelper::args Constant](../vs140/ArgTraitsHelper--args-Constant.md)|Helps [ArgTraits::args](../vs140/ArgTraits--args-Constant.md) keep count of the number of parameters on the Invoke method of a delegate interface.|  
  
## Inheritance Hierarchy  
 `ArgTraitsHelper`  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)