---
title: "Compiler Warning (levels 1 and 4) C4115"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3f94e72-fc49-4d09-b3e7-23d68e61152f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (levels 1 and 4) C4115
'type' : named type definition in parentheses  
  
 The given symbol is used to define a structure, union, or enumerated type inside a parenthetical expression. The scope of the definition may be unexpected.  
  
 In a C function call, the definition has global scope. In a C++ call, the definition has the same scope as the function being called.  
  
 This warning can also be caused by declarators within parentheses (such as prototypes) that are not parenthetical expressions.  
  
 This is a level-1 warning with C++ programs and C programs compiled under ANSI compatibility (/Za). Otherwise, it is level 3.