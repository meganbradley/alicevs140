---
title: "sleep_for Function"
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
ms.assetid: 1175fcb1-1dd5-49ed-8401-de639d878c98
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sleep_for Function
Blocks the calling thread.  
  
## Syntax  
  
```  
template<class Rep,  
class Period>  
inline void sleep_for(  
   const chrono::duration<Rep,  
   Period>& Rel_time  
);  
```  
  
#### Parameters  
 `Rel_time`  
 A [duration](../vs140/duration-Class.md) object that specifies a time interval.  
  
## Remarks  
 The function blocks the calling thread for at least the time that's specified by `Rel_time`. This function does not throw any exceptions.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std::this_thread  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<thread\>](../vs140/-thread-.md)