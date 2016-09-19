---
title: "Compiler Error C2414"
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
ms.assetid: bbe94e03-862e-4990-b15e-544ae464727d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2414
illegal number of operands  
  
### To fix by checking the following possible causes  
  
1.  The opcode does not support the number of operands used. Check an assembly-language reference manual to determine the correct number of operands.  
  
2.  A newer processor supports the instruction with a different number of operands. Adjust the [/arch](../vs140/-arch--Minimum-CPU-Architecture-.md) option to use the later processor.