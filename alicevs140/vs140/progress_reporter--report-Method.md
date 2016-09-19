---
title: "progress_reporter::report Method"
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
ms.assetid: 7d1ea439-0e95-42fa-8bcc-61f06e3c832e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# progress_reporter::report Method
Sends a progress report to the asynchronous action or operation to which this progress reporter is bound.  
  
## Syntax  
  
```  
void report(  
   const _ProgressType& _Val  
) const;  
```  
  
#### Parameters  
 `_Val`  
 The payload to report through a progress notification.  
  
## Requirements  
 **Header:** ppltasks.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [progress_reporter Class](../vs140/progress_reporter-Class.md)