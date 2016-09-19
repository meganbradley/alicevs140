---
title: "SyncLockT::~SyncLockT Destructor"
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
ms.assetid: 9e14870d-017d-45fe-a3dc-cd86b6fa1c3a
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SyncLockT::~SyncLockT Destructor
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
~SyncLockT();  
```  
  
## Remarks  
 Deinitializes an instance of the SyncLockT class.  
  
 This destructor also unlocks the current SyncLockT instance.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::Details  
  
## See Also  
 [SyncLockT Class](../vs140/SyncLockT-Class.md)