---
title: "Compiler Error C2410"
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
ms.assetid: b69b2de1-56f3-4ebc-8913-04ac57ffe8a1
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2410
'identifier' : ambiguous member name in 'context'  
  
 The identifier is a member of more than one structure or union in this context.  
  
 Use a structure or union specifier on the operand that caused the error. A structure or union specifier is an identifier of type `struct` or `union` (a `typedef` name or a variable of the same type as the structure or union being referenced). The specifier must be the left operand of the first member-selection operator (.) to use the operand.