---
title: "CA2218: Override GetHashCode on overriding Equals"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69b020cd-29e8-45a6-952e-32cf3ce2e21d
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2218: Override GetHashCode on overriding Equals
|||  
|-|-|  
|TypeName|OverrideGetHashCodeOnOverridingEquals|  
|CheckId|CA2218|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A public type overrides <xref:System.Object.Equals?qualifyHint=True> but does not override <xref:System.Object.GetHashCode?qualifyHint=True>.  
  
## Rule Description  
 <xref:System.Object.GetHashCode?qualifyHint=False> returns a value, based on the current instance, that is suited for hashing algorithms and data structures such as a hash table. Two objects that are the same type and are equal must return the same hash code to ensure that instances of the following types work correctly:  
  
-   <xref:System.Collections.HashTable?qualifyHint=True>  
  
-   <xref:System.Collections.SortedList?qualifyHint=True>  
  
-   <xref:System.Collections.Generic.Dictionary?qualifyHint=True>  
  
-   <xref:System.Collections.Generic.SortDictionary?qualifyHint=True>  
  
-   <xref:System.Collections.Generic.SortList?qualifyHint=True>  
  
-   <xref:System.Collections.Specialized.HybredDictionary?qualifyHint=True>  
  
-   <xref:System.Collections.Specialized.ListDictionary?qualifyHint=True>  
  
-   <xref:System.Collections.Specialized.OrderedDictionary?qualifyHint=True>  
  
-   Types that implement <xref:System.Collections.Generic.IEqualityComparer?qualifyHint=True>  
  
## How to Fix Violations  
 To fix a violation of this rule, provide an implementation of <xref:System.Object.GetHashCode?qualifyHint=False>. For a pair of objects of the same type, you must ensure that the implementation returns the same value if your implementation of <xref:System.Object.Equals?qualifyHint=False> returns `true` for the pair.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Class Example  
  
### Description  
 The following example shows a class (reference type) that violates this rule.  
  
### Code  
 [!CODE [FxCop.Usage.GetHashCodeErrorClass#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.GetHashCodeErrorClass#1)]  
  
### Comments  
 The following example fixes the violation by overriding <xref:System.Object.GetHashCode?qualifyHint=False>.  
  
### Code  
 [!CODE [FxCop.Usage.GetHashCodeFixedClass#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.GetHashCodeFixedClass#1)]  
  
## Structure Example  
  
### Description  
 The following example shows a structure (value type) that violates this rule.  
  
### Code  
 [!CODE [FxCop.Usage.GetHashCodeErrorStruct#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.GetHashCodeErrorStruct#1)]  
  
### Comments  
 The following example fixes the violation by overriding <xref:System.Object.GetHashCode?qualifyHint=False>.  
  
### Code  
 [!CODE [FxCop.Usage.GetHashCodeFixedStruct#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.GetHashCodeFixedStruct#1)]  
  
## Related Rules  
 [Do not override operator equals on reference types](../vs140/CA1046--Do-not-overload-operator-equals-on-reference-types.md)  
  
 [Operator overloads have named alternates](../vs140/CA2225--Operator-overloads-have-named-alternates.md)  
  
 [Operators should have symmetrical overloads](../vs140/CA2226--Operators-should-have-symmetrical-overloads.md)  
  
 [Override equals on overriding operator equals](../vs140/CA2224--Override-equals-on-overloading-operator-equals.md)  
  
 [Override operator equals on overriding value type equals](../vs140/CA2231--Overload-operator-equals-on-overriding-ValueType.Equals.md)  
  
## See Also  
 <xref:System.Object.Equals?qualifyHint=True>   
 <xref:System.Object.GetHashCode?qualifyHint=True>   
 <xref:System.Collections.HashTable?qualifyHint=True>   
 [Guidelines for Implementing Equals and the Equality Operator (==)](assetId:///bc496a91-fefb-4ce0-ab4c-61f09964119a)