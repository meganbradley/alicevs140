---
title: "CA1721: Property names should not match get methods"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 45a0e853-1f06-4688-af1b-cc634409e295
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1721: Property names should not match get methods
|||  
|-|-|  
|TypeName|PropertyNamesShouldNotMatchGetMethods|  
|CheckId|CA1721|  
|Category|Microsoft.Naming|  
|Breaking Change|Breaking|  
  
## Cause  
 The name of a public or protected member starts with 'Get' and otherwise matches the name of a public or protected property. For example, a type that contains a method that is named 'GetColor' and a property that is named 'Color' violates this rule.  
  
## Rule Description  
 Get methods and properties should have names that clearly distinguish their function.  
  
 Naming conventions provide a common look for libraries that target the common language runtime. This reduces the time that is required to learn a new software library, and increases customer confidence that the library was developed by someone who has expertise in developing managed code.  
  
## How to Fix Violations  
 Change the name so that it does not match the name of a method that is prefixed with 'Get'.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
> [!NOTE]
>  This warning may be excluded if the Get method is caused by implementing IExtenderProvider interface.  
  
## Example  
 The following example contains a method and property that violate this rule.  
  
 [!CODE [FxCop.Naming.GetMethod#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Naming.GetMethod#1)]  
  
## Related Rules  
 [Use properties where appropriate](../vs140/CA1024--Use-properties-where-appropriate.md)