---
title: "duration::operator-= Operator1"
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
H1: duration::operator/= Operator
ms.assetid: dcb9772f-f2d4-41ab-9a5a-bd0df87d0afa
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# duration::operator-= Operator1
Divides the stored tick count by a specified value.  
  
## Syntax  
  
```  
duration& operator/=(const rep& Div);  
```  
  
#### Parameters  
 `Div`  
 A value of the type that is specified by `duration::rep`.  
  
## Return Value  
 The `duration` object after the division is performed.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [duration Class](../vs140/duration-Class.md)   
 [<chrono\>](../vs140/-chrono-.md)