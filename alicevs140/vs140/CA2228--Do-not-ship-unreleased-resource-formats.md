---
title: "CA2228: Do not ship unreleased resource formats"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2c614edc-4e94-4b4f-8067-eea677a75cd9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2228: Do not ship unreleased resource formats
|||  
|-|-|  
|TypeName|DoNotShipUnreleasedResourceFormats|  
|CheckId|CA2228|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A resource file was built using a version of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] that is not currently supported.  
  
## Rule Description  
 Resource files that were built by using pre-release versions of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] might not be usable by supported versions of the .NET Framework.  
  
## How to Fix Violations  
 To fix a violation of this rule, build the resource using a supported version of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]k.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.