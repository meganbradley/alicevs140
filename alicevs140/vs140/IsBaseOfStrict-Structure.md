---
title: "IsBaseOfStrict Structure"
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
ms.assetid: 6fed7366-c8d4-4991-b4fb-43ed93f8e1bf
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IsBaseOfStrict Structure
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   typename Base,  
   typename Derived  
>  
  
struct IsBaseOfStrict;  
template <  
   typename Base  
>  
struct IsBaseOfStrict<Base, Base>;  
```  
  
#### Parameters  
 `Base`  
 The base type.  
  
 `Derived`  
 The derived type.  
  
## Remarks  
 Tests whether one type is the base of another.  
  
 The first template tests whether a type is derived from a base type, which might yield **true** or **false**. The second template tests whether a type is derived from itself, which always yields **false**.  
  
## Members  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|[IsBaseOfStrict::value Constant](../vs140/IsBaseOfStrict--value-Constant.md)|Indicates whether one type is the base of another.|  
  
## Inheritance Hierarchy  
 `IsBaseOfStrict`  
  
## Requirements  
 **Header:** internal.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)