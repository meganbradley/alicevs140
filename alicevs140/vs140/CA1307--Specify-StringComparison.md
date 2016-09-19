---
title: "CA1307: Specify StringComparison"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b0d5e71-1683-4a0d-bc4a-68b2fbd8af71
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1307: Specify StringComparison
|||  
|-|-|  
|TypeName|SpecifyStringComparison|  
|CheckId|CA1307|  
|Category|Microsoft.Globalization|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A string comparison operation uses a method overload that does not set a <xref:System.StringComparison?qualifyHint=False> parameter.  
  
## Rule Description  
 Many string operations, most important the <xref:System.String.Compare?qualifyHint=False> and <xref:System.String.Equals?qualifyHint=False> methods, provide an overload that accepts a <xref:System.StringComparison?qualifyHint=False> enumeration value as a parameter.  
  
 Whenever an overload exists that takes a <xref:System.StringComparison?qualifyHint=False> parameter, it should be used instead of an overload that does not take this parameter. By explicitly setting this parameter, your code is often made clearer and easier to maintain.  
  
## How to Fix Violations  
 To fix a violation of this rule, change string comparison methods to overloads that accept the <xref:System.StringComparison?qualifyHint=False> enumeration as a parameter. For example: change `String.Compare(str1, str2)` to `String.Compare(str1, str2, StringComparison.Ordinal)`.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule when the library or application is intended for a limited local audience and will therefore not be localized.  
  
## See Also  
 [Globalization Warnings](../vs140/Globalization-Warnings.md)   
 [Use ordinal string comparison](../Topic/CA1309:%20Use%20ordinal%20StringComparison.md)