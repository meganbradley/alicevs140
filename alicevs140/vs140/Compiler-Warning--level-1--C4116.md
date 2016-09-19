---
title: "Compiler Warning (level 1) C4116"
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
ms.assetid: 25434ef3-061e-4252-91a5-0fe2a4b2ffb3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4116
unnamed type definition in parentheses  
  
 A structure, union, or enumerated type with no name is defined in a parenthetical expression. The type definition is meaningless.  
  
 In a C function call, the definition has global scope. In a C++ function call, the definition has the same scope as the function being called.