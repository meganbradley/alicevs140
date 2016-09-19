---
title: "Mutex::Lock Method"
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
ms.assetid: 61d95072-b690-441e-a080-0bf94a733141
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mutex::Lock Method
Waits until the current object, or the Mutex object associated with the specified handle, releases the mutex or the specified time-out interval has elapsed.  
  
## Syntax  
  
```  
SyncLock Lock(  
   DWORD milliseconds = INFINITE  
);  
  
static SyncLock Lock(  
   HANDLE h,  
   DWORD milliseconds = INFINITE  
);  
```  
  
#### Parameters  
 `milliseconds`  
 The time-out interval, in milliseconds. The default value is INFINITE, which waits indefinitely.  
  
 `h`  
 The handle of a Mutex object.  
  
## Return Value  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Mutex Class](../vs140/Mutex-Class.md)