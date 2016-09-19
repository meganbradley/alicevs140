---
title: "_ATL_DEBUG_QI"
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
ms.assetid: 4f1feddf-1469-42ad-a2f7-5a816d1c0bc5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_DEBUG_QI
Writes all calls to `QueryInterface` to the output window.  
  
## Syntax  
  
```  
  
#define _ATL_DEBUG_QI  
  
```  
  
## Remarks  
 If a call to `QueryInterface` failed, the output window will display:  
  
 *interface name* - `failed`  
  
## See Also  
 [Debugging and Error Reporting Macros](../vs140/Debugging-and-Error-Reporting-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)