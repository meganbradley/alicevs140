---
title: "Compiler Warning (level 3) CS0675"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 7465dd8d-2543-44f6-b76b-fcae0ef2580d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) CS0675
Bitwise-or operator used on a sign-extended operand; consider casting to a smaller unsigned type first  
  
 The compiler implicitly widened and sign-extended a variable, and then used the resulting value in a bitwise OR operation. This can result in unexpected behavior.  
  
 The following sample generates CS0675:  
  
```  
// CS0675.cs  
// compile with: /W:3  
using System;  
  
public class sign  
{  
   public static void Main()  
   {  
      int hi = 1;  
      int lo = 1;  
      long value = (((long)hi) << 32) | lo;              // CS0675  
      // try the following line instead  
      // long value = (((long)hi) << 32) | ((uint)lo);   // correct  
   }  
}  
```