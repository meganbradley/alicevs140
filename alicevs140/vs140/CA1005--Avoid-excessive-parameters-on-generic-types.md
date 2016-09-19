---
title: "CA1005: Avoid excessive parameters on generic types"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 372b2f28-5c59-4815-9753-6c65b2bb3589
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1005: Avoid excessive parameters on generic types
|||  
|-|-|  
|TypeName|AvoidExcessiveParametersOnGenericTypes|  
|CheckId|CA1005|  
|Category|Microsoft.Design|  
|Breaking Change|Breaking|  
  
## Cause  
 An externally visible generic type has more than two type parameters.  
  
## Rule Description  
 The more type parameters a generic type contains, the more difficult it is to know and remember what each type parameter represents. It is usually obvious with one type parameter, as in `List<T>`, and in certain cases with two type parameters, as in `Dictionary<TKey, TValue>`. If more than two type parameters exist, the difficulty becomes too great for most users (for example, `TooManyTypeParameters<T, K, V>` in C# or `TooManyTypeParameters(Of T, K, V)` in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]).  
  
## How to Fix Violations  
 To fix a violation of this rule, change the design to use no more than two type parameters.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule unless the design absolutely requires more than two type parameters. Providing generics in a syntax that is easy to understand and use reduces the time that is required to learn and increases the adoption rate of new libraries.  
  
## Related Rules  
 [Collections should implement generic interface](../vs140/CA1010--Collections-should-implement-generic-interface.md)  
  
 [Do not declare static members on generic types](../vs140/CA1000--Do-not-declare-static-members-on-generic-types.md)  
  
 [Do not expose generic lists](../Topic/CA1002:%20Do%20not%20expose%20generic%20lists.md)  
  
 [Do not nest generic types in member signatures](../vs140/CA1006--Do-not-nest-generic-types-in-member-signatures.md)  
  
 [Generic methods should provide type parameter](../vs140/CA1004--Generic-methods-should-provide-type-parameter.md)  
  
 [Use generic event handler instances](../Topic/CA1003:%20Use%20generic%20event%20handler%20instances.md)  
  
 [Use generics where appropriate](../Topic/CA1007:%20Use%20generics%20where%20appropriate.md)  
  
## See Also  
 [Generics (C# Programmers Reference)](../Topic/Generics%20\(C%23%20Programming%20Guide\).md)