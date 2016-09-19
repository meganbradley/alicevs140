---
title: "CA2231: Overload operator equals on overriding ValueType.Equals"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 114c0161-261a-40ad-8b2c-0932d6909d2a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2231: Overload operator equals on overriding ValueType.Equals
|||  
|-|-|  
|TypeName|OverloadOperatorEqualsOnOverridingValueTypeEquals|  
|CheckId|CA2231|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A value type overrides <xref:System.Object.Equals?qualifyHint=True> but does not implement the equality operator.  
  
## Rule Description  
 In most programming languages there is no default implementation of the equality operator (==) for value types. If your programming language supports operator overloads, you should consider implementing the equality operator. Its behavior should be identical to that of <xref:System.Object.Equals?qualifyHint=False>.  
  
 You cannot use the default equality operator in an overloaded implementation of the equality operator. Doing so will cause a stack overflow. To implement the equality operator, use the Object.Equals method in your implementation. For example:  
  
```vb  
If (Object.ReferenceEquals(left, Nothing)) Then  
    Return Object.ReferenceEquals(right, Nothing)  
Else  
    Return left.Equals(right)  
End If  
```  
  
```c#  
if (Object.ReferenceEquals(left, null))   
    return Object.ReferenceEquals(right, null);  
return left.Equals(right);  
```  
  
## How to Fix Violations  
 To fix a violation of this rule, implement the equality operator.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule; however, we recommend that you provide the equality operator if possible.  
  
## Example  
 The following example defines a type that violates this rule.  
  
 [!CODE [FxCop.Usage.EqualsGetHashCode#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.EqualsGetHashCode#1)]  
  
## Related Rules  
 [Do not override operator equals on reference types](../vs140/CA1046--Do-not-overload-operator-equals-on-reference-types.md)  
  
 [Operator overloads have named alternates](../vs140/CA2225--Operator-overloads-have-named-alternates.md)  
  
 [Operators should have symmetrical overloads](../vs140/CA2226--Operators-should-have-symmetrical-overloads.md)  
  
 [Override equals on overriding operator equals](../vs140/CA2224--Override-equals-on-overloading-operator-equals.md)  
  
 [Override GetHashCode on overriding Equals](../vs140/CA2218--Override-GetHashCode-on-overriding-Equals.md)  
  
## See Also  
 <xref:System.Object.Equals?qualifyHint=True>