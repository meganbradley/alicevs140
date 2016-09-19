---
title: "HUGE_VAL, _HUGE"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _HUGE
apilocation: 
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 3f044b45-02cd-46b2-b1de-87fd0441dd6a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HUGE_VAL, _HUGE
## Syntax  
  
```  
  
#include <math.h>  
  
```  
  
## Remarks  
 `HUGE_VAL` is the largest representable double value. This value is returned by many run-time math functions when an error occurs. For some functions, –`HUGE_VAL` is returned. `HUGE_VAL` is defined as `_HUGE`, but run-time math functions return `HUGE_VAL`. You should also use `HUGE_VAL` in your code for consistency.  
  
## See Also  
 [Global Constants](../vs140/Global-Constants.md)