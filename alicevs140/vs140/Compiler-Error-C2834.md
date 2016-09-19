---
title: "Compiler Error C2834"
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
ms.assetid: 28f9f6eb-ab2a-4e64-aaaa-9d14f955de41
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2834
'operator operator' must be globally qualified  
  
 The `new` and `delete` operators are tied to the class where they reside. Scope resolution cannot be used to select a version of `new` or `delete` from a different class. To implement multiple forms of the `new` or `delete` operator, create a version of the operator with extra formal parameters.