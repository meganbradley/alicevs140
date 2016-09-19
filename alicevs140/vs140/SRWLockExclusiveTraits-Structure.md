---
title: "SRWLockExclusiveTraits Structure"
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
ms.assetid: 38a996ef-c2d7-4886-b413-a426ecee8f05
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SRWLockExclusiveTraits Structure
Describes common characteristics of the SRWLock class in exclusive lock mode.  
  
## Syntax  
  
```  
struct SRWLockExclusiveTraits;  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`Type`|Synonym for a pointer to the [SRWLOCK](../vs140/SRWLock-Class.md) class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[SRWLockExclusiveTraits::GetInvalidValue Method](../vs140/SRWLockExclusiveTraits--GetInvalidValue-Method.md)|Retrieves an SRWLockExclusiveTraits object that is always invalid.|  
|[SRWLockExclusiveTraits::Unlock Method](../vs140/SRWLockExclusiveTraits--Unlock-Method.md)|Releases exclusive control of the specified SRWLock object.|  
  
## Inheritance Hierarchy  
 `SRWLockExclusiveTraits`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## See Also  
 [HandleTraits Namespace](../vs140/Microsoft--WRL--Wrappers--HandleTraits-Namespace.md)