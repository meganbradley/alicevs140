---
title: "CA2112: Secured types should not expose fields"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9eb13a78-3487-49f2-81d1-3c3866db132f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2112: Secured types should not expose fields
|||  
|-|-|  
|TypeName|SecuredTypesShouldNotExposeFields|  
|CheckId|CA2112|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A public or protected type contains public fields and is secured by a [link demand](assetId:///a33fd5f9-2de9-4653-a4f0-d9df25082c4d).  
  
## Rule Description  
 If code has access to an instance of a type that is secured by a link demand, the code does not have to satisfy the link demand to access the type's fields.  
  
## How to Fix Violations  
 To fix a violation of this rule, make the fields nonpublic and add public properties or methods that return the field data. LinkDemand security checks on types protect access to the type's properties and methods. However, code access security does not apply to fields.  
  
## When to Suppress Warnings  
 Both for security issues and for good design, you should fix violations by making the public fields nonpublic. You can suppress a warning from this rule if the field does not hold information that should remain secured, and you do not rely on the contents of the field.  
  
## Example  
 The following example is composed of a library type (`SecuredTypeWithFields`) with unsecured fields, a type (`Distributor`) that can create instances of the library type and mistaken passes instances to types do not have permission to create them, and application code that can read an instance's fields even though it does not have the permission that secures the type.  
  
 The following library code violates the rule.  
  
 [!CODE [FxCop.Security.LinkDemandOnField#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Security.LinkDemandOnField#1)]  
  
## Example  
 The application cannot create an instance because of the link demand that protects the secured type. The following class enables the application to obtain an instance of the secured type.  
  
 [!CODE [FxCop.Security.LDOnFieldsDistributor#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Security.LDOnFieldsDistributor#1)]  
  
## Example  
 The following application illustrates how, without permission to access a secured type's methods, code can access its fields.  
  
 [!CODE [FxCop.Security.TestLinkDemandOnFields#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Security.TestLinkDemandOnFields#1)]  
  
 This example produces the following output.  
  
 **Creating an instance of SecuredTypeWithFields.**  
**Secured type fields: 22, 33**  
**Changing secured type's field...**  
**Cached Object fields: 99, 33**   
## Related Rules  
 [Do not declare visible instance fields](../vs140/CA1051--Do-not-declare-visible-instance-fields.md)  
  
## See Also  
 [Link Demands](assetId:///a33fd5f9-2de9-4653-a4f0-d9df25082c4d)   
 [Security Demands](assetId:///8c37635d-e2c1-4b64-a258-61d9e87405e6)