---
title: "CA2214: Do not call overridable methods in constructors"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 335b57ca-a6e8-41b4-a20e-57ee172c97c3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2214: Do not call overridable methods in constructors
|||  
|-|-|  
|TypeName|DoNotCallOverridableMethodsInConstructors|  
|CheckId|CA2214|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 The constructor of an unsealed type calls a virtual method defined in its class.  
  
## Rule Description  
 When a virtual method is called, the actual type that executes the method is not selected until run time. When a constructor calls a virtual method, it is possible that the constructor for the instance that invokes the method has not executed.  
  
## How to Fix Violations  
 To fix a violation of this rule, do not call a type's virtual methods from within the type's constructors.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule. The constructor should be redesigned to eliminate the call to the virtual method.  
  
## Example  
 The following example demonstrates the effect of violating this rule. The test application creates an instance of `DerivedType`, which causes its base class (`BadlyConstructedType`) constructor to execute. `BadlyConstructedType`'s constructor incorrectly calls the virtual method `DoSomething`. As the output shows, `DerivedType.DoSomething()` executes, and does so before `DerivedType`'s constructor executes.  
  
 [!CODE [FxCop.Usage.CtorVirtual#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.CtorVirtual#1)]  
  
 This example produces the following output.  
  
 **Calling base ctor.**  
**Derived DoSomething is called - initialized ? No**  
**Calling derived ctor.**