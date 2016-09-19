---
title: "CA2131: Security critical types may not participate in type equivalence"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4170f3b1-6086-430d-8fba-837d5538c573
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2131: Security critical types may not participate in type equivalence
|||  
|-|-|  
|TypeName|CriticalTypesMustNotParticipateInTypeEquivalence|  
|CheckId|CA2131|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A type participates in type equivalence and a either the type itself, or a member or field of the type, is marked with the <xref:System.Security.SecurityCriticalAttribute?qualifyHint=False> attribute.  
  
## Rule Description  
 This rule fires on any critical types or types that contain critical methods or fields that are participating in type equivalence. When the CLR detects such a type, it fails to load it with a <xref:System.TypeLoadException?qualifyHint=False> at run time. Typically, this rule fires only when users implement type equivalence manually rather than by relying on tlbimp and the compilers to do the type equivalence.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove the SecurityCritical attribute.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The following examples demonstrate an interface, a method, and a field that will cause this rule to fire.  
  
 [!CODE [FxCop.Security.CA2131.CriticalTypesMustNotParticipateInTypeEquivalence#1](../CodeSnippet/VS_Snippets_CodeAnalysis/fxcop.security.ca2131.criticaltypesmustnotparticipateintypeequivalence#1)]  
  
## See Also  
 [Security-Transparent Code, Level 2](assetId:///4d05610a-0da6-4f08-acea-d54c9d6143c0)