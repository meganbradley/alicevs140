---
title: "CDC::QueryAbort"
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
ms.assetid: 24c23370-94e2-433c-a886-89755c3ce7e3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::QueryAbort
Calls the abort function installed by the [SetAbortProc](../vs140/CDC--SetAbortProc.md) member function for a printing application and queries whether the printing should be terminated.  
  
## Syntax  
  
```  
  
BOOL QueryAbort( ) const;  
```  
  
## Return Value  
 The return value is nonzero if printing should continue or if there is no abort procedure. It is 0 if the print job should be terminated. The return value is supplied by the abort function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetAbortProc](../vs140/CDC--SetAbortProc.md)