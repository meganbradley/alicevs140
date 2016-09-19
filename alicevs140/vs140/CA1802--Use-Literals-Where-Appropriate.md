---
title: "CA1802: Use Literals Where Appropriate"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2515e4cd-9e61-486d-b067-58ba1a743ce4
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1802: Use Literals Where Appropriate
|||  
|-|-|  
|TypeName|UseLiteralsWhereAppropriate|  
|CheckId|CA1802|  
|Category|Microsoft.Performance|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A field is declared `static` and `readonly` (`Shared` and `ReadOnly` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]), and is initialized with a value that is computable at compile time.  
  
## Rule Description  
 The value of a `static``readonly` field is computed at runtime when the static constructor for the declaring type is called. If the `static``readonly` field is initialized when it is declared and a static constructor is not declared explicitly, the compiler emits a static constructor to initialize the field.  
  
 The value of a `const` field is computed at compile time and stored in the metadata, which increases runtime performance when it is compared to a `static``readonly` field.  
  
 Because the value assigned to the targeted field is computable at compile time, change the declaration to a `const` field so that the value is computed at compile time instead of at runtime.  
  
## How to Fix Violations  
 To fix a violation of this rule, replace the `static` and `readonly` modifiers with the `const` modifier.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule, or disable the rule, if performance is not of concern.  
  
## Example  
 The following example shows a type, `UseReadOnly`, that violates the rule and a type, `UseConstant`, that satisfies the rule.  
  
 [!CODE [FxCop.Performance.UseLiterals#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Performance.UseLiterals#1)]