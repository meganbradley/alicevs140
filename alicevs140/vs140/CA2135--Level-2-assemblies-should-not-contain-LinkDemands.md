---
title: "CA2135: Level 2 assemblies should not contain LinkDemands"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7a775285-42d2-4f13-8434-3fdb0deeebe6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2135: Level 2 assemblies should not contain LinkDemands
|||  
|-|-|  
|TypeName|SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands|  
|CheckId|CA2135|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A class or class member is using a <xref:System.Security.Permissions.SecurityAction.LinkDemand?qualifyHint=False> in an application that is using Level 2 security.  
  
## Rule Description  
 LinkDemands are deprecated in the level 2 security rule set. Instead of using LinkDemands to enforce security at just-in-time (JIT) compilation time, mark the methods, types, and fields with the <xref:System.Security.SecurityCriticalAttribute?qualifyHint=False> attribute.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove the <xref:System.Security.Permissions.SecurityAction.LinkDemand?qualifyHint=False> and mark the type or member with the <xref:System.Security.SecurityCriticalAttribute?qualifyHint=False> attribute.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 In the following example, the <xref:System.Security.Permissions.SecurityAction.LinkDemand?qualifyHint=False> should be removed and the method marked with the <xref:System.Security.SecurityCriticalAttribute?qualifyHint=False> attribute.  
  
 [!CODE [FxCop.Security.CA2135.SecurityRuleSetLevel2MethodsShouldNotBeProtectedWithLinkDemands#1](../CodeSnippet/VS_Snippets_CodeAnalysis/fxcop.security.ca2135.securityrulesetlevel2methodsshouldnotbeprotectedwithlinkdemands#1)]