---
title: "Compiler Warning (level 1) C4124"
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
ms.assetid: c08c3a65-9584-47a1-a147-44f00c4b230e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4124
__fastcall with stack checking is inefficient  
  
 The `__fastcall` keyword was used with stack checking enabled.  
  
 The `__fastcall` convention generates faster code, but stack checking causes slower code. When using `__fastcall`, turn off stack checking with the **check_stack** pragma or /Gs.  
  
 This warning is issued only for the first function declared under these conditions.