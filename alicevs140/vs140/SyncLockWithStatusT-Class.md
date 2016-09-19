---
title: "SyncLockWithStatusT Class"
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
ms.assetid: 4832fd93-0ac8-4168-9404-b43fefea7476
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SyncLockWithStatusT Class
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   typename SyncTraits  
>  
class SyncLockWithStatusT : public SyncLockT<SyncTraits>;  
```  
  
#### Parameters  
 `SyncTraits`  
 A type that can take exclusive or shared ownership of a resource.  
  
## Remarks  
 Represents a type that can take exclusive or shared ownership of a resource.  
  
 The SyncLockWithStatusT class is used to implement the [Mutex](../vs140/Mutex-Class.md) and [Semaphore](../vs140/Semaphore-Class.md) classes.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockWithStatusT::SyncLockWithStatusT Constructor](../vs140/SyncLockWithStatusT--SyncLockWithStatusT-Constructor.md)|Initializes a new instance of the SyncLockWithStatusT class.|  
  
### Protected Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockWithStatusT::SyncLockWithStatusT Constructor](../vs140/SyncLockWithStatusT--SyncLockWithStatusT-Constructor.md)|Initializes a new instance of the SyncLockWithStatusT class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockWithStatusT::GetStatus Method](../vs140/SyncLockWithStatusT--GetStatus-Method.md)|Retrieves the wait status of the current SyncLockWithStatusT object.|  
|[SyncLockWithStatusT::IsLocked Method](../vs140/SyncLockWithStatusT--IsLocked-Method.md)|Indicates whether the current SyncLockWithStatusT object owns a resource; that is, the SyncLockWithStatusT object is *locked*.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockWithStatusT::status_ Data Member](../vs140/SyncLockWithStatusT--status_-Data-Member.md)|Holds the result of the underlying wait operation after a lock operation on an object based on the current SyncLockWithStatusT object.|  
  
## Inheritance Hierarchy  
 `SyncLockT`  
  
 `SyncLockWithStatusT`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::Details  
  
## See Also  
 [Microsoft::WRL::Wrappers::Details Namespace](../vs140/Microsoft--WRL--Wrappers--Details-Namespace.md)