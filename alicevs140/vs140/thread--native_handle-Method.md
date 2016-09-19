---
title: "thread::native_handle Method"
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
ms.topic: article
ms.assetid: 9853a0c5-4ea4-4063-b7a5-88b6283ccfdc
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# thread::native_handle Method
Returns the implementation-specific type that represents the thread handle. The thread handle can be used in implementation-specific ways.  
  
## Syntax  
  
```  
native_handle_type native_handle();  
```  
  
## Return Value  
 `native_handle_type` is defined as a Win32 `HANDLE` that's cast as `void *`.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [thread Class](../vs140/thread-Class.md)   
 [<thread\>](../vs140/-thread-.md)