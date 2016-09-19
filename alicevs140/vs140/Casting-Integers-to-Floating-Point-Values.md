---
title: "Casting Integers to Floating-Point Values"
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
ms.assetid: 81fd5b7d-15eb-4c11-a8c8-e1621ff54fd3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Casting Integers to Floating-Point Values
**ANSI 3.2.1.3** The direction of truncation when an integral number is converted to a floating-point number that cannot exactly represent the original value  
  
 When an integral number is cast to a floating-point value that cannot exactly represent the value, the value is rounded (up or down) to the nearest suitable value.  
  
 For example, casting an **unsigned long** (with 32 bits of precision) to a **float** (whose mantissa has 23 bits of precision) rounds the number to the nearest multiple of 256. The **long** values 4,294,966,913 to 4,294,967,167 are all rounded to the **float** value 4,294,967,040.  
  
## See Also  
 [Floating-Point Math](../vs140/Floating-Point-Math.md)