---
title: "Portability Warnings"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 902e859a-2153-4970-baaa-8a5b4a11806f
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Portability Warnings
Portability warnings support portability across different operating systems.  
  
## In This Section  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1900: Value type fields should be portable](../vs140/CA1900--Value-type-fields-should-be-portable.md)|This rule checks that structures that are declared by using an explicit layout attribute will align correctly when marshaled to unmanaged code on 64-bit operating systems.|  
|[CA1901: P/Invoke declarations should be portable](../vs140/CA1901--P-Invoke-declarations-should-be-portable.md)|This rule evaluates the size of each parameter and the return value of a P/Invoke, and verifies that their size is correct when marshaled to unmanaged code on 32-bit and 64-bit operating systems.|  
|[CA1903: Use only API from targeted framework](../vs140/CA1903--Use-only-API-from-targeted-framework.md)|A member or type is using a member or type that was introduced in a service pack that was not included together with the targeted framework of the project.|