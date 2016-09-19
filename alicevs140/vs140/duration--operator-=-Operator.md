---
title: "duration::operator*= Operator"
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
ms.assetid: 1c2c381e-2ca4-4900-956b-1848b193c065
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration::operator*= Operator
Multiplies the stored tick count by a specified value.  
  
## Syntax  
  
```  
duration& operator*=(const rep& Mult);  
```  
  
#### Parameters  
 `Mult`  
 A value of the type that is specified by `duration::rep`.  
  
## Return Value  
 The `duration` object after the multiplication is performed.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [duration Class](../vs140/duration-Class.md)   
 [<chrono\>](../vs140/-chrono-.md)