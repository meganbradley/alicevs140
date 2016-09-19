---
title: "Compiler Error C2021"
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
ms.assetid: 064f32e2-3794-48d5-9767-991003dcb36a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2021
expected exponent value, not 'character'  
  
 The character used as the exponent of a floating-point constant is not a valid number. Be sure to use an exponent that is in range.  
  
## Example  
 The following sample generates C2021:  
  
```  
// C2021.cpp  
float test1=1.175494351E;   // C2021  
```  
  
## Example  
 Possible resolution:  
  
```  
// C2021b.cpp  
// compile with: /c  
float test2=1.175494351E8;  
```