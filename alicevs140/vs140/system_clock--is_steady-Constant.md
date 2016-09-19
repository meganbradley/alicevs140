---
title: "system_clock::is_steady Constant"
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
ms.assetid: 87f8b689-a8e4-4ae0-86ea-01dbd588ef6f
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# system_clock::is_steady Constant
Static value that specifies whether the clock type is *steady*.  
  
## Syntax  
  
```  
static const bool is_steady = false;  
```  
  
## Return Value  
 In this implementation, `system_clock::is_steady` always returns `false`.  
  
## Remarks  
 A clock is *steady* if it is [monotonic](../vs140/system_clock--is_monotonic-Constant.md) and if the time between clock ticks is constant.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [system_clock Structure](../vs140/system_clock-Structure.md)   
 [<chrono\>](../vs140/-chrono-.md)