---
title: "CriticalSection Class"
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
ms.assetid: f2e0a024-71a3-4f6b-99ea-d93a4a608ac4
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CriticalSection Class
Represents a critical section object.  
  
## Syntax  
  
```  
class CriticalSection;  
```  
  
## Members  
  
### Constructor  
  
|Name|Description|  
|----------|-----------------|  
|[CriticalSection::CriticalSection Constructor](../vs140/CriticalSection--CriticalSection-Constructor.md)|Initializes a synchronization object that is similar to a mutex object, but can be used by only the threads of a single process.|  
|[CriticalSection::~CriticalSection Destructor](../vs140/CriticalSection--~CriticalSection-Destructor.md)|Deinitializes and destroys the current CriticalSection object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CriticalSection::TryLock Method](../vs140/CriticalSection--TryLock-Method.md)|Attempts to enter a critical section without blocking. If the call is successful, the calling thread takes ownership of the critical section.|  
|[CriticalSection::Lock Method](../vs140/CriticalSection--Lock-Method.md)|Waits for ownership of the specified critical section object. The function returns when the calling thread is granted ownership.|  
|[CriticalSection::IsValid Method](../vs140/CriticalSection--IsValid-Method.md)|Indicates whether the current critical section is valid.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CriticalSection::cs_ Data Member](../vs140/CriticalSection--cs_-Data-Member.md)|Declares a critical section data member.|  
  
## Inheritance Hierarchy  
 `CriticalSection`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Microsoft::WRL::Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)