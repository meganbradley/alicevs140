---
title: "SyncLockT::SyncLockT Constructor"
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
ms.assetid: 713dfd9f-7369-4d86-b4a0-8b32c184d89b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SyncLockT::SyncLockT Constructor
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
SyncLockT(  
   _Inout_ SyncLockT&& other  
);  
  
explicit SyncLockT(  
   typename SyncTraits::Type sync = SyncTraits::GetInvalidValue()  
);  
```  
  
#### Parameters  
 `other`  
 An rvalue-reference to another SyncLockT object.  
  
 `sync`  
 A reference to another SyncLockWithStatusT object.  
  
## Remarks  
 Initializes a new instance of the SyncLockT class.  
  
 The first constructor initializes the current SyncLockT object from another SyncLockT object specified by parameter `other`, and then invalidates the other SyncLockT object. The second constructor is `protected`, and initializes the current SyncLockT object to an invalid state.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::Details  
  
## See Also  
 [SyncLockT Class](../vs140/SyncLockT-Class.md)