---
title: "duration::operator-- Operator"
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
ms.assetid: 5b6bbc73-9ed0-43dc-a467-008335186bf6
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration::operator-- Operator
Decrements the stored tick count.  
  
## Syntax  
  
```  
duration& operator--();  
duration operator--(int);  
```  
  
## Return Value  
 The first method returns `*this`.  
  
 The second method returns a copy of `*this` that is made before the decrement.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [duration Class](../vs140/duration-Class.md)   
 [<chrono\>](../vs140/-chrono-.md)