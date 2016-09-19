---
title: "HANDLENullTraits Structure"
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
ms.assetid: 88a29a14-c516-40cb-a0ca-ee897a668623
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HANDLENullTraits Structure
Defines common characteristics of an uninitialized handle.  
  
## Syntax  
  
```  
struct HANDLENullTraits;  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`Type`|A synonym for HANDLE.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[HANDLENullTraits::Close Method](../vs140/HANDLENullTraits--Close-Method.md)|Closes the specified handle.|  
|[HANDLENullTraits::GetInvalidValue Method](../vs140/HANDLENullTraits--GetInvalidValue-Method.md)|Represents an invalid handle.|  
  
## Inheritance Hierarchy  
 `HANDLENullTraits`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## See Also  
 [HandleTraits Namespace](../vs140/Microsoft--WRL--Wrappers--HandleTraits-Namespace.md)