---
title: "CA1010: Collections should implement generic interface"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c7d7126f-fa70-40be-8f93-3243e1760dc5
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1010: Collections should implement generic interface
|||  
|-|-|  
|TypeName|CollectionsShouldImplementGenericInterface|  
|CheckId|CA1010|  
|Category|Microsoft.Design|  
|Breaking Change|Non-breaking|  
  
## Cause  
 An externally visible type implements the <xref:System.Collections.IEnumerable?qualifyHint=True> interface but does not implement the <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=True> interface, and the containing assembly targets [!INCLUDE[dnprdnlong](../vs140/includes/dnprdnlong_md.md)]. This rule ignores types that implement <xref:System.Collections.IDictionary?qualifyHint=True>.  
  
## Rule Description  
 To broaden the usability of a collection, implement one of the generic collection interfaces. Then the collection can be used to populate generic collection types such as the following:  
  
-   <xref:System.Collections.Generic.List`1?qualifyHint=True>  
  
-   <xref:System.Collections.Generic.Queue`1?qualifyHint=True>  
  
-   <xref:System.Collections.Generic.Stack`1?qualifyHint=True>  
  
## How to Fix Violations  
 To fix a violation of this rule, implement one of the following generic collection interfaces:  
  
-   <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=True>  
  
-   <xref:System.Collections.Generic.ICollection`1?qualifyHint=True>  
  
-   <xref:System.Collections.Generic.IList`1?qualifyHint=True>  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule; however, the collection will have a more limited use.  
  
## Example Violation  
  
### Description  
 The following example shows a class (reference type) that derives from the non-generic `CollectionBase` class, which violates this rule.  
  
### Code  
 [!CODE [FxCop.Design.CollectionsGenericViolation#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Design.CollectionsGenericViolation#1)]  
  
### Comments  
 To fix a violation of this violation, you should either implement the generic interfaces or change the base class to a type that already implements both the generic and non-generic interfaces, such as the `Collection<T>` class.  
  
## Fix by Base Class Change  
  
### Description  
 The following example fixes the violation by changing the base class of the collection from the non-generic `CollectionBase` class to the generic `Collection<T>` (`Collection(Of T)` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]) class.  
  
### Code  
 [!CODE [FxCop.Design.CollectionsGenericBase#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Design.CollectionsGenericBase#1)]  
  
### Comments  
 Changing the base class of an already released class is considered a breaking change to existing consumers.  
  
## Fix by Interface Implementation  
  
### Description  
 The following example fixes the violation by implementing these generic interfaces: `IEnumerable<T>`, `ICollection<T>`, and `IList<T>` (`IEnumerable(Of T)`, `ICollection(Of T)`, and `IList(Of T)` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]).  
  
### Code  
 [!CODE [FxCop.Design.CollectionsGenericInterface#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Design.CollectionsGenericInterface#1)]  
  
## Related Rules  
 [Avoid excessive parameters on generic types](../vs140/CA1005--Avoid-excessive-parameters-on-generic-types.md)  
  
 [Do not declare static members on generic types](../vs140/CA1000--Do-not-declare-static-members-on-generic-types.md)  
  
 [Do not expose generic lists](../Topic/CA1002:%20Do%20not%20expose%20generic%20lists.md)  
  
 [Do not nest generic types in member signatures](../vs140/CA1006--Do-not-nest-generic-types-in-member-signatures.md)  
  
 [Generic methods should provide type parameter](../vs140/CA1004--Generic-methods-should-provide-type-parameter.md)  
  
 [Use generic event handler instances](../Topic/CA1003:%20Use%20generic%20event%20handler%20instances.md)  
  
 [Use generics where appropriate](../Topic/CA1007:%20Use%20generics%20where%20appropriate.md)  
  
## See Also  
 [Generics (C# Programmers Reference)](../Topic/Generics%20\(C%23%20Programming%20Guide\).md)