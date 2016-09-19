---
title: "CA1000: Do not declare static members on generic types"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5c0da594-f8d0-4f40-953d-56bf7fbd2087
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1000: Do not declare static members on generic types
|||  
|-|-|  
|TypeName|DoNotDeclareStaticMembersOnGenericTypes|  
|CheckId|CA1000|  
|Category|Microsoft.Design|  
|Breaking Change|Breaking|  
  
## Cause  
 An externally visible generic type contains a `static` (`Shared` in Visual Basic) member.  
  
## Rule Description  
 When a `static` member of a generic type is called, the type argument must be specified for the type. When a generic instance member that does not support inference is called, the type argument must be specified for the member. The syntax for specifying the type argument in these two cases is different and easily confused, as the following calls demonstrate:  
  
```vb  
' Shared method in a generic type.  
GenericType(Of Integer).SharedMethod()  
  
' Generic instance method that does not support inference.  
someObject.GenericMethod(Of Integer)()  
```  
  
```c#  
// Static method in a generic type.  
GenericType<int>.StaticMethod();  
  
// Generic instance method that does not support inference.  
someObject.GenericMethod<int>();  
```  
  
 Generally, both of the prior declarations should be avoided so that the type argument does not have to be specified when the member is called. This results in a syntax for calling members in generics that is no different from the syntax for non-generics. For more information, see [Generic methods should provide type parameter](../vs140/CA1004--Generic-methods-should-provide-type-parameter.md).  
  
## How to Fix Violations  
 To fix a violation of this rule, remove the static member or change it to an instance member.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule. Providing generics in a syntax that is easy to understand and use reduces the time that is required to learn and increases the adoption rate of new libraries.  
  
## Related Rules  
 [Avoid excessive parameters on generic types](../vs140/CA1005--Avoid-excessive-parameters-on-generic-types.md)  
  
 [Collections should implement generic interface](../vs140/CA1010--Collections-should-implement-generic-interface.md)  
  
 [Do not expose generic lists](../Topic/CA1002:%20Do%20not%20expose%20generic%20lists.md)  
  
 [Do not nest generic types in member signatures](../vs140/CA1006--Do-not-nest-generic-types-in-member-signatures.md)  
  
 [Generic methods should provide type parameter](../vs140/CA1004--Generic-methods-should-provide-type-parameter.md)  
  
 [Use generic event handler instances](../Topic/CA1003:%20Use%20generic%20event%20handler%20instances.md)  
  
 [Use generics where appropriate](../Topic/CA1007:%20Use%20generics%20where%20appropriate.md)  
  
## See Also  
 [Generics (C# Programmers Reference)](../Topic/Generics%20\(C%23%20Programming%20Guide\).md)