---
title: "Compiler Error C3550"
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
ms.topic: error-reference
ms.assetid: 9f2d5ffc-e429-41a1-89e3-7acc4fd47e14
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3550
only plain 'decltype(auto)' is allowed in this context  
  
 If `decltype(auto)` is used as a placeholder for the return type of a function, it must be used by itself. It cannot be used as part of a pointer declaration (`decltype(auto*)`), a reference declaration (`decltype(auto&)`), or any other such qualification.  
  
## See Also  
 [auto Keyword (Type Deduction)](../vs140/auto--C---.md)