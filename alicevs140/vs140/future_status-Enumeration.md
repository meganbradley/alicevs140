---
title: "future_status Enumeration"
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
ms.assetid: efd78076-0959-4e85-963f-c7f16fdff84a
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# future_status Enumeration
Supplies symbolic names for the reasons that a timed wait function can return.  
  
## Syntax  
  
```  
enum future_status{    ready,    timeout,    deferred};  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`deferred`|The *associated asynchronous state* holds a *deferred function* that's not running.|  
|`ready`|The associated asynchronous state is *ready*.|  
|`timeout`|The time limit was reached.|  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std::future_status  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<future\>](../vs140/-future-.md)