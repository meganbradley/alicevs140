---
title: "CA1053: Static holder types should not have constructors"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10302b9a-fa5e-4935-a06a-513d9600f613
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1053: Static holder types should not have constructors
|||  
|-|-|  
|TypeName|StaticHolderTypesShouldNotHaveConstructors|  
|CheckId|CA1053|  
|Category|Microsoft.Design|  
|Breaking Change|Breaking|  
  
## Cause  
 A public or nested public type declares only static members and has a public or protected default constructor.  
  
## Rule Description  
 The constructor is unnecessary because calling static members does not require an instance of the type. Also, because the type does not have non-static members, creating an instance does not provide access to any of the type's members.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove the default constructor or make it private.  
  
> [!NOTE]
>  Some compilers automatically create a public default constructor if the type does not define any constructors. If this is the case with your type, add a private default constructor to eliminate the violation.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule. The presence of the constructor suggests that the type is not a static type.  
  
## Example  
 The following example shows a type that violates this rule. Notice that there is no default constructor in the source code. When this code is compiled into an assembly, the C# compiler will insert a default constructor, which will violate this rule. To correct this, declare a private constructor.  
  
 [!CODE [FxCop.Design.StaticTypes#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Design.StaticTypes#1)]