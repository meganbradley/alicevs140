---
title: "Compiler Warning (level 4) C4092"
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
ms.assetid: 396ae826-a892-4327-bd66-f4762376d72b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4092
sizeof returns 'unsigned long'  
  
 The operand of the `sizeof` operator was very large, so `sizeof` returned an unsigned **long**. This warning occurs under the Microsoft extensions ([/Ze](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)). Under ANSI compatibility (/Za), the result is truncated instead.