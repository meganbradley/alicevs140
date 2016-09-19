---
title: "Compiler Error C2041"
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
ms.assetid: c9a33bb1-f9cf-47d6-bd21-7d867a8c37d5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2041
illegal digit 'character' for base 'number'  
  
 The specified character is not a valid digit for the base (such as octal or hex).  
  
 The following sample generates C2041:  
  
```  
// C2041.cpp  
int i = 081;   // C2041  8 is not a base 8 digit  
```  
  
 Possible resolution:  
  
```  
// C2041b.cpp  
// compile with: /c  
int j = 071;  
```