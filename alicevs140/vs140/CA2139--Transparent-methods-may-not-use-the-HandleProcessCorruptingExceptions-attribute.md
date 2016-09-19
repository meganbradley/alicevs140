---
title: "CA2139: Transparent methods may not use the HandleProcessCorruptingExceptions attribute"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 45a0328a-add7-40f9-8934-dff59beb02b3
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2139: Transparent methods may not use the HandleProcessCorruptingExceptions attribute
|||  
|-|-|  
|TypeName|TransparentMethodsMustNotHandleProcessCorruptingExceptions|  
|CheckId|CA2139|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A transparent method is marked with the <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?qualifyHint=False> attribute.  
  
## Rule Description  
 This rule fires any method which is transparent and attempts to handle a process corrupting exception by using the <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?qualifyHint=False> attribute. A process corrupting exception is a CLR version 4.0 exception classification of exceptions such <xref:System.AccessViolationException?qualifyHint=False>. The HandleProcessCorruptedStateExceptionsAttribute attribute may only be used by security critical methods, and will be ignored if it is applied to a transparent method. To handle process corrupting exceptions, this method must become security critical or security safe-critical.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove the <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?qualifyHint=False> attribute, or mark the method with the <xref:System.Security.SecurityCriticalAttribute?qualifyHint=False> or the <xref:System.Security.SecuritySafeCriticalAttribute?qualifyHint=False> attribute.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 In this example, a transparent method is marked with the <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?qualifyHint=False> attribute and will fail the rule. The method should also be marked with the <xref:System.Security.SecurityCriticalAttribute?qualifyHint=False> or the <xref:System.Security.SecuritySafeCriticalAttribute?qualifyHint=False> attribute.  
  
 [!CODE [FxCop.Security.CA2139.TransparentMethodsMustNotHandleProcessCorruptingExceptions#1](../CodeSnippet/VS_Snippets_CodeAnalysis/fxcop.security.ca2139.transparentmethodsmustnothandleprocesscorruptingexceptions#1)]