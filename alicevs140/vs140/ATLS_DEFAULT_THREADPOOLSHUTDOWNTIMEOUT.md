---
title: "ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT"
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
ms.assetid: c1e660a7-d490-42af-bbe1-ded76e80cc10
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT
This macro defines the default time in milliseconds that [CThreadPool](../vs140/CThreadPool-Class.md) will wait for a thread to shut down.  
  
## Syntax  
  
```  
  
#define ATLS_DEFAULT_THREADPOOLSHUTDOWNTIMEOUT  
  
```  
  
## Remarks  
 The default time is 36 seconds. If necessary, you can define your own positive integer value for this symbol before including atlutil.h.  
  
 To set the timeout at run time or for a particular object, call [CThreadPool::SetTimeout](../vs140/CThreadPool--SetTimeout.md).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)