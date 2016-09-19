---
title: "Expression Evaluator Error CXX0065"
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
ms.assetid: aac68f87-0b90-4c19-afa6-1c587625a5fd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression Evaluator Error CXX0065
variable needs stack frame  
  
 An expression contained a variable that exists within the current scope but hasn't been created yet.  
  
 This error can occur when you have stepped into the prolog of a function but not yet set up the stack frame for the function, or if you have stepped into the exit code for the function.  
  
 Step through the prolog code until the stack frame has been set up before evaluating the expression.  
  
 This error is identical to CAN0065.