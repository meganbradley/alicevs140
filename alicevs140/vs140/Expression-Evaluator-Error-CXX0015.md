---
title: "Expression Evaluator Error CXX0015"
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
ms.assetid: 35efaf77-d578-48d8-bfc5-fdeb2a46a8b5
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression Evaluator Error CXX0015
expression too complex (stack overflow)  
  
 The expression entered was too complex or nested too deeply for the amount of storage available to the C expression evaluator.  
  
 Overflow usually occurs because of too many pending calculations.  
  
 Rearrange the expression so that each component of the expression can be evaluated as it is encountered, rather than having to wait for other parts of the expression to be calculated.  
  
 Break the expression into multiple commands.  
  
 This error is identical to CAN0015.