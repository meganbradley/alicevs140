---
title: "SRWLockSharedTraits Structure"
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
ms.assetid: 709cb51e-d70c-40b6-bdb4-d8eacf3af495
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SRWLockSharedTraits Structure
Describes common characteristics of the SRWLock class in shared lock mode.  
  
## Syntax  
  
```  
struct SRWLockSharedTraits;  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`Type`|Synonym for a pointer to the [SRWLOCK](../vs140/SRWLock-Class.md) class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[SRWLockSharedTraits::GetInvalidValue Method](../vs140/SRWLockSharedTraits--GetInvalidValue-Method.md)|Retrieves an SRWLockSharedTraits object that is always invalid.|  
|[SRWLockSharedTraits::Unlock Method](../vs140/SRWLockSharedTraits--Unlock-Method.md)|Releases exclusive control of the specified SRWLock object.|  
  
## Inheritance Hierarchy  
 `SRWLockSharedTraits`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## See Also  
 [HandleTraits Namespace](../vs140/Microsoft--WRL--Wrappers--HandleTraits-Namespace.md)