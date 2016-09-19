---
title: "duration::operator= Operator"
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
ms.assetid: 4485ff11-5a68-46c8-98ca-cd2c6952a712
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration::operator= Operator
Reduces the stored tick count modulo a specified value.  
  
## Syntax  
  
```  
duration& operator%=(  
   const rep& Div  
);  
duration& operator%=(  
   const duration& Div  
);  
```  
  
#### Parameters  
 `Div`  
 For the first method, `Div` represents a tick count. For the second method, `Div` is a `duration` object that contains a tick count.  
  
## Return Value  
 The `duration` object after the modulo operation is performed.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [duration Class](../vs140/duration-Class.md)   
 [<chrono\>](../vs140/-chrono-.md)