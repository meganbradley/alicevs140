---
title: "Compiler Error C2828"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: d8df6ed4-5954-46c2-b59b-52881d4e923d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2828
'operator operator' cannot be globally overridden with binary form  
  
 The operator cannot have a binary form outside of an object.  
  
### To fix by using the following possible solutions  
  
1.  Make the overloaded operator local to an object.  
  
2.  Choose an appropriate unary operator to overload.