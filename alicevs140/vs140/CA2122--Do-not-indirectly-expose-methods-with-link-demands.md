---
title: "CA2122: Do not indirectly expose methods with link demands"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3eda58e7-c6ec-41c3-8112-ae0841109c6a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2122: Do not indirectly expose methods with link demands
|||  
|-|-|  
|TypeName|DoNotIndirectlyExposeMethodsWithLinkDemands|  
|CheckId|CA2122|  
|Category|Microsoft.Security|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A public or protected member has a [link demand](assetId:///a33fd5f9-2de9-4653-a4f0-d9df25082c4d) and is called by a member that does not perform any security checks.  
  
## Rule Description  
 A link demand checks the permissions of the immediate caller only. If a member `X` makes no security demands of its callers, and calls code protected by a link demand, a caller without the necessary permission can use `X` to access the protected member.  
  
## How to Fix Violations  
 Add a security [demand](assetId:///8c37635d-e2c1-4b64-a258-61d9e87405e6) or link demand to the member so that it no longer provides unsecured access to the link demand-protected member.  
  
## When to Suppress Warnings  
 To safely suppress a warning from this rule, you must make sure that your code does not grant its callers access to operations or resources that can be used in a destructive manner.  
  
## Example  
 The following examples show a library that violates the rule, and an application that demonstrates the library's weakness. The sample library provides two methods that together violate the rule. The `EnvironmentSetting` method is secured by a link demand for unrestricted access to environment variables. The `DomainInformation` method makes no security demands of its callers before it calls `EnvironmentSetting`.  
  
 [!CODE [FxCop.Security.UnsecuredDoNotCall#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Security.UnsecuredDoNotCall#1)]  
  
## Example  
 The following application calls the unsecured library member.  
  
 [!CODE [FxCop.Security.TestUnsecuredDoNot1#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Security.TestUnsecuredDoNot1#1)]  
  
 This example produces the following output.  
  
 **Value from unsecured member: seattle.corp.contoso.com**   
## See Also  
 [Secure Coding Guidelines](assetId:///4f882d94-262b-4494-b0a6-ba9ba1f5f177)   
 [Link Demands](assetId:///a33fd5f9-2de9-4653-a4f0-d9df25082c4d)   
 [Demands](assetId:///8c37635d-e2c1-4b64-a258-61d9e87405e6)