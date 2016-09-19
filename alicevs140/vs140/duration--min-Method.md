---
title: "duration::min Method"
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
ms.assetid: 7a07bd74-028c-4d17-9df2-4ead5181107b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration::min Method
Static method that returns the lower bound for values of template parameter type `Ref`.  
  
## Syntax  
  
```  
static constexpr duration min();  
```  
  
## Return Value  
 In effect, returns `duration(duration_values<rep>::min())`.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [duration Class](../vs140/duration-Class.md)   
 [duration_values Structure](../vs140/duration_values-Structure.md)   
 [<chrono\>](../vs140/-chrono-.md)