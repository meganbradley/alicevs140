---
title: "critical_section::native_handle Method"
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
ms.assetid: c02a87a4-9673-4467-ba48-efc7c69af52d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# critical_section::native_handle Method
Returns a platform specific native handle, if one exists.  
  
## Syntax  
  
```  
native_handle_type native_handle();  
```  
  
## Return Value  
 A reference to the critical section.  
  
## Remarks  
 A `critical_section` object is not associated with a platform specific native handle for the Windows operating system. The method simply returns a reference to the object itself.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [critical_section Class](../vs140/critical_section-Class.md)