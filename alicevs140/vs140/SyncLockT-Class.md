---
title: "SyncLockT Class"
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
ms.assetid: a967f6f7-3555-43d1-b210-2bb65d63d15e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SyncLockT Class
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template <  
   typename SyncTraits  
>  
class SyncLockT;  
```  
  
#### Parameters  
 `SyncTraits`  
 The type that can take ownership of a resource.  
  
## Remarks  
 Represents a type that can take exclusive or shared ownership of a resource.  
  
 The SyncLockT class is used, for example, to help implement the [SRWLock](../vs140/SRWLock-Class.md) class.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockT::SyncLockT Constructor](../vs140/SyncLockT--SyncLockT-Constructor.md)|Initializes a new instance of the SyncLockT class.|  
|[SyncLockT::~SyncLockT Destructor](../vs140/SyncLockT--~SyncLockT-Destructor.md)|Deinitializes an instance of the SyncLockT class.|  
  
### Protected Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockT::SyncLockT Constructor](../vs140/SyncLockT--SyncLockT-Constructor.md)|Initializes a new instance of the SyncLockT class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockT::IsLocked Method](../vs140/SyncLockT--IsLocked-Method.md)|Indicates whether the current SyncLockT object owns a resource; that is, the SyncLockT object is *locked*.|  
|[SyncLockT::Unlock Method](../vs140/SyncLockT--Unlock-Method.md)|Releases control of the resource held by the current SyncLockT object, if any.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[SyncLockT::sync_ Data Member](../vs140/SyncLockT--sync_-Data-Member.md)|Holds the underlying resource represented by the SyncLockT class.|  
  
## Inheritance Hierarchy  
 `SyncLockT`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::Details  
  
## See Also  
 [Microsoft::WRL::Wrappers::Details Namespace](../vs140/Microsoft--WRL--Wrappers--Details-Namespace.md)   
 [SRWLock Class](../vs140/SRWLock-Class.md)