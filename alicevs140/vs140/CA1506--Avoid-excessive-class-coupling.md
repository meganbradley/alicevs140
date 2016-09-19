---
title: "CA1506: Avoid excessive class coupling"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9f0943c0-e802-4e3f-8798-2ab8653ddc80
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1506: Avoid excessive class coupling
|||  
|-|-|  
|TypeName|AvoidExcessiveClassCoupling|  
|CheckId|CA1506|  
|Category|Microsoft.Maintainability|  
|Breaking Change|Breaking|  
  
## Cause  
 A type or method is coupled with many other types.  
  
## Rule Description  
 This rule measures class coupling by counting the number of unique type references that a type or method contains.  
  
 Types and methods that have a high degree of class coupling can be difficult to maintain. It is a good practice to have types and methods that exhibit low coupling and high cohesion.  
  
## How to Fix Violations  
 To fix this violation, try to redesign the type or method to reduce the number of types to which it is coupled.  
  
## When to Suppress Warnings  
 Exclude this warning when the type or method is still considered maintainable despite its large number of dependencies on other types.  
  
## See Also  
 [Maintainability Warnings](../vs140/Maintainability-Warnings.md)   
 [Measuring Complexity and Maintainability of Managed Code](../vs140/Measuring-Complexity-and-Maintainability-of-Managed-Code.md)