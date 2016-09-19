---
title: "CA1800: Do not cast unnecessarily"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b79a010a-6627-421e-8955-6007e32fa808
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1800: Do not cast unnecessarily
|||  
|-|-|  
|TypeName|DoNotCastUnnecessarily|  
|CheckId|CA1800|  
|Category|Microsoft.Performance|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A method performs duplicate casts on one of its arguments or local variables. For complete analysis by this rule, the tested assembly must be built by using debugging information and the associated program database (.pdb) file must be available.  
  
## Rule Description  
 Duplicate casts decrease performance, especially when the casts are performed in compact iteration statements. For explicit duplicate cast operations, store the result of the cast in a local variable and use the local variable instead of the duplicate cast operations.  
  
 If the C# `is` operator is used to test whether the cast will succeed before the actual cast is performed, consider testing the result of the `as` operator instead. This provides the same functionality without the implicit cast operation that is performed by the `is` operator.  
  
## How to Fix Violations  
 To fix a violation of this rule, modify the method implementation to minimize the number of cast operations.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule, or to ignore the rule completely, if performance is not a concern.  
  
## Example  
 The following example shows a method that violates the rule by using the C# `is` operator. A second method satisfies the rule by replacing the `is` operator with a test against the result of the `as` operator, which decreases the number of cast operations per iteration from two to one.  
  
 [!CODE [FxCop.Performance.UnnecessaryCastsAsIs#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Performance.UnnecessaryCastsAsIs#1)]  
  
## Example  
 The following example shows a method, `start_Click`, that has multiple duplicate explicit casts, which violates the rule, and a method, `reset_Click`, which satisfies the rule by storing the cast in a local variable.  
  
 [!CODE [FxCop.Performance.UnnecessaryCasts#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Performance.UnnecessaryCasts#1)]  
  
## See Also  
 [C# as Operator](../vs140/as--C#-Reference-.md)   
 [C# is Operator](../vs140/is--C#-Reference-.md)