---
title: "ATLS_DEFAULT_THREADSPERPROC"
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
ms.assetid: e0dcf107-72a9-4122-abb4-83c63aa7d571
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLS_DEFAULT_THREADSPERPROC
This macro defines the default number of threads per processor used by [CThreadPool](../vs140/CThreadPool-Class.md).  
  
## Syntax  
  
```  
  
#define ATLS_DEFAULT_THREADSPERPROC  
  
```  
  
## Remarks  
 The default is 2 threads per processor. If necessary, you can define your own positive integer value for this symbol before including atlutil.h.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)