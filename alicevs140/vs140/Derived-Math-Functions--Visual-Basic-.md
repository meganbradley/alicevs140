---
title: "Derived Math Functions (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 63e449d8-9444-44fb-8db1-6d9cf346e2aa
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Derived Math Functions (Visual Basic)
The following table shows non-intrinsic math functions that can be derived from the intrinsic math functions of the <xref:System.Math?qualifyHint=True> object. You can access the intrinsic math functions by adding `Imports System.Math` to your file or project.  
  
|Function|Derived equivalents|  
|--------------|-------------------------|  
|Secant (Sec(x))|1 / Cos(x)|  
|Cosecant (Csc(x))|1 / Sin(x)|  
|Cotangent (Ctan(x))|1 / Tan(x)|  
|Inverse sine (Asin(x))|Atan(x / Sqrt(-x * x + 1))|  
|Inverse cosine (Acos(x))|Atan(-x / Sqrt(-x * x + 1)) + 2 \* Atan(1)|  
|Inverse secant (Asec(x))|2 * Atan(1) – Atan(Sign(x) / Sqrt(x \* x – 1))|  
|Inverse cosecant (Acsc(x))|Atan(Sign(x) / Sqrt(x * x – 1))|  
|Inverse cotangent (Acot(x))|2 * Atan(1) - Atan(x)|  
|Hyperbolic sine (Sinh(x))|(Exp(x) – Exp(-x)) / 2|  
|Hyperbolic cosine (Cosh(x))|(Exp(x) + Exp(-x)) / 2|  
|Hyperbolic tangent (Tanh(x))|(Exp(x) – Exp(-x)) / (Exp(x) + Exp(-x))|  
|Hyperbolic secant (Sech(x))|2 / (Exp(x) + Exp(-x))|  
|Hyperbolic cosecant (Csch(x))|2 / (Exp(x) – Exp(-x))|  
|Hyperbolic cotangent (Coth(x))|(Exp(x) + Exp(-x)) / (Exp(x) – Exp(-x))|  
|Inverse hyperbolic sine (Asinh(x))|Log(x + Sqrt(x * x + 1))|  
|Inverse hyperbolic cosine (Acosh(x))|Log(x + Sqrt(x * x – 1))|  
|Inverse hyperbolic tangent (Atanh(x))|Log((1 + x) / (1 – x)) / 2|  
|Inverse hyperbolic secant (AsecH(x))|Log((Sqrt(-x * x + 1) + 1) / x)|  
|Inverse hyperbolic cosecant (Acsch(x))|Log((Sign(x) * Sqrt(x \* x + 1) + 1) / x)|  
|Inverse hyperbolic cotangent (Acoth(x))|Log((x + 1) / (x – 1)) / 2|  
  
## See Also  
 [Math Functions](../vs140/Math-Functions--Visual-Basic-.md)