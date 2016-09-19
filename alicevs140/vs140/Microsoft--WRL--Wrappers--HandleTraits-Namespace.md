---
title: "Microsoft::WRL::Wrappers::HandleTraits Namespace"
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
ms.assetid: 2fb5c6d1-bfc2-4e09-91eb-31705064ffb3
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Microsoft::WRL::Wrappers::HandleTraits Namespace
Describes characteristics of common handle-based resource types.  
  
## Syntax  
  
```  
namespace Microsoft::WRL::Wrappers::HandleTraits;  
```  
  
## Members  
  
### Structures  
  
|Name|Description|  
|----------|-----------------|  
|[CriticalSectionTraits Structure](../vs140/CriticalSectionTraits-Structure.md)|Specializes a `CriticalSection` object to support either an invalid critical section or a function to release a critical section.|  
|[EventTraits Structure](../vs140/EventTraits-Structure.md)|Defines characteristics of an `Event` class handle.|  
|[FileHandleTraits Structure](../vs140/FileHandleTraits-Structure.md)|Defines characteristics of a file handle.|  
|[HANDLENullTraits Structure](../vs140/HANDLENullTraits-Structure.md)|Defines common characteristics of an uninitialized handle.|  
|[HANDLETraits Structure](../vs140/HANDLETraits-Structure.md)|Defines common characteristics of a handle.|  
|[MutexTraits Structure](../vs140/MutexTraits-Structure.md)|Defines common characteristics of the [Mutex](../vs140/Mutex-Class.md) class.|  
|[SemaphoreTraits Structure](../vs140/SemaphoreTraits-Structure.md)|Defines common characteristics of a Semaphore object.|  
|[SRWLockExclusiveTraits Structure](../vs140/SRWLockExclusiveTraits-Structure.md)|Describes common characteristics of the `SRWLock` class in exclusive lock mode.|  
|[SRWLockSharedTraits Structure](../vs140/SRWLockSharedTraits-Structure.md)|Describes common characteristics of the `SRWLock` class in shared lock mode.|  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)