---
title: "DA0010: Expensive GetHashCode"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3987e21a-5b4f-45e4-8a33-6b3f0a472c08
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DA0010: Expensive GetHashCode
|||  
|-|-|  
|Rule Id|DA0010|  
|Category|.NET Framework Usage|  
|Profiling methods|Sampling<br /><br /> .NET Memory|  
|Message|GetHashCode functions should be cheap and not allocate any memory. Reduce complexity of hash code function if possible.|  
|Message type|Warning|  
  
## Cause  
 Calls to the GetHashCode method of the type are a significant proportion of the profiling data or the method allocates memory.  
  
## Rule Description  
 Hashing is a technique for rapidly locating a particular item in a large collection. Because hash tables can be very large and have to support very high rates of access,  hash tables should be extremely efficient. An implication of this requirement is that GetHashCode methods in the .NET Framework should not allocate memory. Allocating memory increases the load on the garbage collector and exposes the method to potential delays if it become necessary to run garbage collection as a result of the allocation request.  
  
## How to Fix Violations  
 Reduce the complexity of the method.