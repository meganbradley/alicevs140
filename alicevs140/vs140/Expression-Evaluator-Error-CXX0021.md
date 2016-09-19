---
title: "Expression Evaluator Error CXX0021"
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
ms.assetid: d6c0c35a-16c2-42c0-a7d2-e910350a47f0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression Evaluator Error CXX0021
struct or union used as scalar  
  
 A structure or union was used in an expression, but no element was specified.  
  
 When manipulating a structure or union variable, the name of the variable may appear by itself, without a field qualifier. If a structure or union is used in an expression, it must be qualified with the specific element desired.  
  
 Specify the element whose value is to be used in the expression.  
  
 This error is identical to CAN0021.