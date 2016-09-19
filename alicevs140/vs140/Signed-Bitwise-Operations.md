---
title: "Signed Bitwise Operations"
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
ms.assetid: 1e5cf65b-ee32-41a0-a5c2-82c1854091f6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Signed Bitwise Operations
**ANSI 3.3** The results of bitwise operations on signed integers  
  
 Bitwise operations on signed integers work the same as bitwise operations on unsigned integers. For example, `–16 & 99` can be expressed in binary as  
  
```  
  11111111 11110000  
& 00000000 01100011  
  _________________  
  00000000 01100000  
```  
  
 The result of the bitwise AND is 96.  
  
## See Also  
 [Integers](../vs140/Integers.md)