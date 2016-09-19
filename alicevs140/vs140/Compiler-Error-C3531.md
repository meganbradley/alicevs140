---
title: "Compiler Error C3531"
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
ms.assetid: 2bdb9fdc-9ddf-403e-8b92-02763d434487
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3531
'symbol': a symbol whose type contains 'auto' must have an initializer  
  
 The specified variable does not have an initializer expression.  
  
### To correct this error  
  
1.  Specify an initializer expression, such as a simple assignment that uses equal-sign syntax, when you declare the variable.  
  
## Example  
 The following example yields C3531 because variables `x1`, `y1, y2, y3`, and `z2` are not initialized.  
  
```  
// C3531.cpp  
// Compile with /Zc:auto  
int main()  
{  
   auto x1;                  // C3531  
   auto y1, y2, y3;          // C3531  
   auto z1 = 1, z2, z3 = -1; // C3531  
   return 0;  
}  
```  
  
## See Also  
 [auto Keyword](../vs140/auto-Keyword.md)