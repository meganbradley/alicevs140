---
title: "MutexTraits Structure"
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
ms.assetid: 6582df80-b9ba-4892-948f-d572a3b23d54
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MutexTraits Structure
Defines common characteristics of the [Mutex](../vs140/Mutex-Class.md) class.  
  
## Syntax  
  
```  
struct MutexTraits : HANDLENullTraits;  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[MutexTraits::Unlock Method](../vs140/MutexTraits--Unlock-Method.md)|Releases exclusive control of a shared resource.|  
  
## Inheritance Hierarchy  
 `HANDLENullTraits`  
  
 `MutexTraits`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## See Also  
 [HandleTraits Namespace](../vs140/Microsoft--WRL--Wrappers--HandleTraits-Namespace.md)