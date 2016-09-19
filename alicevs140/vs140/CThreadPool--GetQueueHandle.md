---
title: "CThreadPool::GetQueueHandle"
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
ms.assetid: 039c5ba7-d769-4ed7-86a9-840e40f0f967
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CThreadPool::GetQueueHandle
Call this method to get the handle of the IO completion port used to queue work items.  
  
## Syntax  
  
```  
  
HANDLE GetQueueHandle( ) throw( );  
  
```  
  
## Return Value  
 Returns the queue handle or NULL if the thread pool has not been initialized.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CThreadPool Class](../vs140/CThreadPool-Class.md)