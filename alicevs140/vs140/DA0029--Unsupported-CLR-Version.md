---
title: "DA0029: Unsupported CLR Version"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76247259-c6f3-44c4-b3f9-d8dac16b5e0d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DA0029: Unsupported CLR Version
|||  
|-|-|  
|Rule Id|DA0029|  
|Category|Profiling Tools Usage|  
|Profiling method|Profiling from the command line|  
|Message|An unsupported CLR version was detected during collection. Managed symbols may not resolve correctly.|  
|Rule type|Information.|  
  
## Cause  
 You are trying to profile an application that uses the [!INCLUDE[net_v11_long](../vs140/includes/net_v11_long_md.md)] that is not supported by the Profiling Tools.  
  
## Rule Description  
 This warning occurs because the profiling tools will be unable to resolve symbols for the managed code running in the application. The profiling tools cannot resolve managed code symbols for applications that are running the [!INCLUDE[net_v11_long](../vs140/includes/net_v11_long_md.md)].  
  
## How to Fix Violations  
 None.