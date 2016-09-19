---
title: "Mutex Class"
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
ms.assetid: 682a0963-721c-46a2-8871-000e9997505b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mutex Class
Represents a synchronization object that exclusively controls a shared resource.  
  
## Syntax  
  
```  
class Mutex : public HandleT<HandleTraits::MutexTraits>  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|**SyncLock**|A synonym for a class that supports synchronous locks.|  
  
### Public Constructor  
  
|Name|Description|  
|----------|-----------------|  
|[Mutex::Mutex Constructor](../vs140/Mutex--Mutex-Constructor.md)|Initializes a new instance of the Mutex class.|  
  
### Public Members  
  
|Name|Description|  
|----------|-----------------|  
|[Mutex::Lock Method](../vs140/Mutex--Lock-Method.md)|Waits until the current object, or the Mutex object associated with the specified handle, releases the mutex or the specified time-out interval has elapsed.|  
  
### Public Operator  
  
|Name|Description|  
|----------|-----------------|  
|[Mutex::operator= Operator](../vs140/Mutex--operator=-Operator.md)|Assigns (moves) the specified Mutex object to the current Mutex object.|  
  
## Inheritance Hierarchy  
 `Mutex`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Microsoft::WRL::Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)