---
title: "Compiler Error C2545"
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
ms.assetid: 51598eb9-0c57-4306-a0cd-3862980f3672
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2545
'operator' : unable to find overloaded operator  
  
 The operator cannot be used with the operands provided. You must supply an overloaded operator with the required operands.  
  
 This error can be caused if operands have incorrect type.  
  
 This error may be fixed if you define a conversion operator or constructor that takes a single parameter.