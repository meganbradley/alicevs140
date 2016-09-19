---
title: "MemoryTypeEnum"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8778c047-edeb-4495-8f9f-3f8bbb297099
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MemoryTypeEnum
Specifies the type of memory to access.  
  
## Syntax  
  
```cpp#  
enum MemoryTypeEnum {  
   MemTypeCode,  
   MemTypeData,  
   MemTypeStack,  
   MemTypeAny = -1  
};  
```  
  
#### Parameters  
 `MemTypeCode`  
 Accesses only code memory.  
  
 `MemTypeData`  
 Accesses data or stack memory.  
  
 `MemTypeStack`  
 Accesses only stack memory.  
  
 `MemTypeAny`  
 Accesses any kind of memory.  
  
## Remarks  
 The values in this enumeration are passed to the [IDiaStackWalkHelper::readMemory](../vs140/IDiaStackWalkHelper--readMemory.md) method to limit access to different types of memory.  
  
## Requirements  
 Header: cvconst.h  
  
## See Also  
 [Enumerations and Structures](../vs140/Enumerations-and-Structures.md)   
 [IDiaStackWalkHelper::readMemory Method](../vs140/IDiaStackWalkHelper--readMemory.md)