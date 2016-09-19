---
title: "Fatal Error C1054"
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
ms.assetid: 9cfb7307-b22a-4418-b7c0-2621b0ab5b1b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1054
compiler limit : initializers nested too deeply  
  
 The code exceeds the nesting limit on initializers (10-15 levels, depending on the combination of types being initialized).  
  
### To fix by using the following possible solutions  
  
1.  Simplify the data types being initialized to reduce nesting.  
  
2.  Initialize variables in separate statements after the declaration.