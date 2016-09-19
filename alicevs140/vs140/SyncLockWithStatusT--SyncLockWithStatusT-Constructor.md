---
title: "SyncLockWithStatusT::SyncLockWithStatusT Constructor"
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
ms.assetid: 5d2fb820-ae1b-495f-8084-ebb4fecc3104
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SyncLockWithStatusT::SyncLockWithStatusT Constructor
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
SyncLockWithStatusT(  
   _Inout_ SyncLockWithStatusT&& other  
);  
  
explicit SyncLockWithStatusT(  
   typename SyncTraits::Type sync,  
   DWORD status  
);  
```  
  
#### Parameters  
 `other`  
 An rvalue-reference to another SyncLockWithStatusT object.  
  
 `sync`  
 A reference to another SyncLockWithStatusT object.  
  
 `status`  
 The value of the [status_](../vs140/SyncLockWithStatusT--status_-Data-Member.md) data member of the `other` parameter or the `sync` parameter.  
  
## Remarks  
 Initializes a new instance of the SyncLockWithStatusT class.  
  
 The first constructor initializes the current SyncLockWithStatusT object from another SyncLockWithStatusT specified by parameter `other`, and then invalidates the other SyncLockWithStatusT object. The second constructor is `protected`, and initializes the current SyncLockWithStatusT object to an invalid state.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::Details  
  
## See Also  
 [SyncLockWithStatusT Class](../vs140/SyncLockWithStatusT-Class.md)   
 [SyncLockWithStatusT::GetStatus Method](../vs140/SyncLockWithStatusT--GetStatus-Method.md)