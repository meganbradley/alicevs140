---
title: "CA1026: Default parameters should not be used"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 09643415-36ef-4d0f-9411-5721e14e2512
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1026: Default parameters should not be used
|||  
|-|-|  
|TypeName|DefaultParametersShouldNotBeUsed|  
|CheckId|CA1026|  
|Category|Microsoft.Design|  
|Breaking Change|Breaking|  
  
## Cause  
 An externally visible type contains an externally visible method that uses a default parameter.  
  
## Rule Description  
 Methods that use default parameters are allowed under the Common Language Specification (CLS); however, the CLS allows compilers to ignore the values that are assigned to these parameters. Code that is written for compilers that ignore default parameter values must explicitly provide arguments for each default parameter. To maintain the behavior that you want across programming languages, methods that use default parameters should be replaced with method overloads that provide the default parameters.  
  
 The compiler ignores the values of default parameters for Managed Extension for C++ when it accesses managed code. The Visual Basic compiler supports methods that have default parameters that use the [Optional](../vs140/Optional--Visual-Basic-.md) keyword.  
  
## How to Fix Violations  
 To fix a violation of this rule, replace the method that uses default parameters with method overloads that supply the default parameters.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The following example shows a method that uses default parameters, and the overloaded methods that provide an equivalent functionality.  
  
 [!CODE [FxCop.Design.DefaultParameters#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Design.DefaultParameters#1)]  
  
## Related Rules  
 [Replace repetitive arguments with params array](../Topic/CA1025:%20Replace%20repetitive%20arguments%20with%20params%20array.md)  
  
## See Also  
 [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6)