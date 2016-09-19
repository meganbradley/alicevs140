---
title: "Compiler Error C2415"
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
ms.assetid: f225c913-2bea-46b1-b096-3d358ac94a15
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2415
improper operand type  
  
 The opcode does not use operands of this type.  
  
### To fix by checking the following possible causes  
  
1.  The opcode does not support the number of operands used. Check an assembly-language reference manual to determine the correct number of operands.  
  
2.  A newer processor supports the instruction with additional types. Adjust the [/arch](../vs140/-arch--Minimum-CPU-Architecture-.md) option to use the later processor.