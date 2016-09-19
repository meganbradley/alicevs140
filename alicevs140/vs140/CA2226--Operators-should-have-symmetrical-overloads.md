---
title: "CA2226: Operators should have symmetrical overloads"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d202401a-ea14-4559-b15e-0ea4f5b68789
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2226: Operators should have symmetrical overloads
|||  
|-|-|  
|TypeName|OperatorsShouldHaveSymmetricalOverloads|  
|CheckId|CA2226|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A type implements the equality or inequality operator and does not implement the opposite operator.  
  
## Rule Description  
 There are no circumstances where either equality or inequality is applicable to instances of a type, and the opposite operator is undefined. Types typically implement the inequality operator by returning the negated value of the equality operator.  
  
 The C# compiler issues an error for violations of this rule.  
  
## How to Fix Violations  
 To fix a violation of this rule, implement both the equality and inequality operators, or remove the one that is present.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule. Your type will not work in a manner that is consistent with the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)].  
  
## Related Rules  
 [Do not override operator equals on reference types](../vs140/CA1046--Do-not-overload-operator-equals-on-reference-types.md)  
  
 [Operator overloads have named alternates](../vs140/CA2225--Operator-overloads-have-named-alternates.md)  
  
 [Override equals on overriding operator equals](../vs140/CA2224--Override-equals-on-overloading-operator-equals.md)  
  
 [Override GetHashCode on overriding Equals](../vs140/CA2218--Override-GetHashCode-on-overriding-Equals.md)  
  
 [Override operator equals on overriding value type equals](../vs140/CA2231--Overload-operator-equals-on-overriding-ValueType.Equals.md)