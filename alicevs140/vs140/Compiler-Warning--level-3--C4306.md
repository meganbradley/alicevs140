---
title: "Compiler Warning (level 3) C4306"
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
ms.assetid: 5b2192d7-402d-4b6d-8619-08105e7dcac7
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4306
**'**   
 ***identifier* ' : conversion from '**   
 ***type1* ' to '**   
 ***type2* ' of greater size**  
  
 The identifier is type cast to a larger pointer. The unfilled high bits of the new type will be zero-filled.  
  
 This warning may indicate an unwanted conversion. The resulting pointer may not be valid.