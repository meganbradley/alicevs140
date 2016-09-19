---
title: "CA1410: COM registration methods should be matched"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3b2e62d-fd66-4093-9f0c-dba01ad995fd
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA1410: COM registration methods should be matched
|||  
|-|-|  
|TypeName|ComRegistrationMethodsShouldBeMatched|  
|CheckId|CA1410|  
|Category|Microsoft.Interoperability|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A type declares a method that is marked with the <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?qualifyHint=True> attribute but does not declare a method that is marked with the <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?qualifyHint=True> attribute, or vice versa.  
  
## Rule Description  
 For Component Object Model (COM) clients to create a [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] type, the type must first be registered. If it is available, a method that is marked with the <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?qualifyHint=False> attribute is called during the registration process to run user-specified code. A corresponding method that is marked with the <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?qualifyHint=False> attribute is called during the unregistration process to reverse the operations of the registration method.  
  
## How to Fix Violations  
 To fix a violation of this rule, add the corresponding registration or unregistration method.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The following example shows a type that violates the rule. The commented code shows the fix for the violation.  
  
 [!CODE [FxCop.Interoperability.ComRegistration#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Interoperability.ComRegistration#1)]  
  
## Related Rules  
 [Com registration methods should not be visible](../Topic/CA1411:%20COM%20registration%20methods%20should%20not%20be%20visible.md)  
  
## See Also  
 <xref:System.Runtime.InteropServices.RegistrationServices?qualifyHint=True>   
 [Registering Assemblies with COM](assetId:///87925795-a3ae-4833-b138-125413478551)   
 [Assembly Registration Tool (Regasm.exe)](assetId:///e190e342-36ef-4651-a0b4-0e8c2c0281cb)