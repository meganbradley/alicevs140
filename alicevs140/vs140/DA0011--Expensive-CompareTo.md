---
title: "DA0011: Expensive CompareTo"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 239a381d-0d97-4367-8668-746c93f5af2c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DA0011: Expensive CompareTo
|||  
|-|-|  
|Rule Id|DA0011|  
|Category|.NET Framework Usage|  
|Profiling methods|Sampling<br /><br /> .NET Memory|  
|Message|CompareTo functions should be cheap and not allocate any memory. Reduce complexity of CompareTo function if possible.|  
|Rule type|Warning|  
  
## Cause  
 The CompareTo method of the type is expensive or allocates memory.  
  
## Rule Description  
 CompareTo methods should be efficient and should not allocate memory.  
  
## How to Fix Violations  
 Reduce the complexity of the CompareTo method.