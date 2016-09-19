---
title: "CA1055: URI return values should not be strings"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40e39873-7872-4988-8195-9eb0ade9ece0
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1055: URI return values should not be strings
|||  
|-|-|  
|TypeName|UriReturnValuesShouldNotBeStrings|  
|CheckId|CA1055|  
|Category|Microsoft.Design|  
|Breaking Change|Breaking|  
  
## Cause  
 The name of a method contains "uri", "Uri", "urn", "Urn", "url", or "Url", and the method returns a string.  
  
## Rule Description  
 This rule splits the method name into tokens based on the Pascal casing convention and checks whether each token equals "uri", "Uri", "urn", "Urn", "url", or "Url". If there is a match, the rule assumes that the method returns a uniform resource identifier (URI). A string representation of a URI is prone to parsing and encoding errors, and can lead to security vulnerabilities. The <xref:System.Uri?qualifyHint=True> class provides these services in a safe and secure manner.  
  
## How to Fix Violations  
 To fix a violation of this rule, change the return type to a <xref:System.Uri?qualifyHint=False>.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule if the return value does not represent a URI.  
  
## Example  
 The following example shows a type, `ErrorProne`, that violates this rule, and a type, `SaferWay`, that satisfies the rule.  
  
 [!CODE [FxCop.Design.UriNotString#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString#1)]  
  
## Related Rules  
 [Uri properties should not be strings](../vs140/CA1056--URI-properties-should-not-be-strings.md)  
  
 [Uri parameters should not be strings](../vs140/CA1054--URI-parameters-should-not-be-strings.md)  
  
 [Pass system uri objects instead of strings](../vs140/CA2234--Pass-System.Uri-objects-instead-of-strings.md)  
  
 [String uri overloads call system uri overloads](../Topic/CA1057:%20String%20URI%20overloads%20call%20System.Uri%20overloads.md)