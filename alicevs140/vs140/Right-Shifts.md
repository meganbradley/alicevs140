---
title: "Right Shifts"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c878e97d-ea3c-4c6b-90a8-b1b24b2d5b19
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Right Shifts
The result of a right shift of a negative-value signed integral type  
  
 Shifting a negative value to the right yields half the absolute value, rounded down. For example, a signed `short` value of –253 (hex 0xFF03, binary 11111111 00000011) shifted right one bit produces –127 (hex 0xFF81, binary 11111111 10000001). A positive 253 shifted right produces +126.  
  
 Right shifts preserve the sign bit of signed integral types. When a signed integer shifts right, the most-significant bit remains set. For example, if 0xF0000000 is a signed `int`, a right shift produces 0xF8000000. Shifting a negative `int` right 32 times produces 0xFFFFFFFF.  
  
 When an unsigned integer shifts right, the most-significant bit is cleared. For example, if 0xF000 is unsigned, the result is 0x7800. Shifting an `unsigned` or positive `int` right 32 times produces 0x00000000.  
  
## See Also  
 [Integers](../vs140/Integers.md)