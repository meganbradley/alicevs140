---
title: "Compiler Error C3558"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 429be117-f78f-421e-a1a8-181026759fa0
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3558
'typename': a lambda return type cannot contain 'auto'  
  
 The return type for a lambda expression cannot contain the `auto` type specifier. For example, the following code fragment yields error C3558.  
  
```  
[]() -> auto {}; // C3558  
```  
  
## See Also  
 [auto Keyword (Type Deduction)](../vs140/auto--C---.md)   
 [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md)