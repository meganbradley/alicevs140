---
title: "AsyncTaskMethodBuilder Structure - Internal Members"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f32f5857-7ef8-45fd-8b5a-7f644eb98b11
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# AsyncTaskMethodBuilder Structure - Internal Members
This topic describes the internal members of the <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder?qualifyHint=False> class. For general information about this class, see the <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder?qualifyHint=False> reference topic.  
  
 **Namespace:** <xref:System.Runtime.CompilerServices?qualifyHint=True>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
 Because you cannot access these internal members from the .NET Framework, the following syntax is provided in Common Intermediate Language (CIL).  
  
## Syntax  
  
```  
.class public sequential ansi sealed beforefieldinit System.Runtime.CompilerServices.AsyncTaskMethodBuilder  
       extends System.ValueType  
       implements System.Runtime.CompilerServices.IAsyncMethodBuilder  
```  
  
## Internal Members  
  
|Name|Description|  
|----------|-----------------|  
|[ObjectIdForDebugger property](../Topic/AsyncTaskMethodBuilder.ObjectIdForDebugger%20Property.md)|Gets an object that may be used to uniquely identify this builder to the debugger.|  
|[m_builder field](../vs140/AsyncTaskMethodBuilder.m_builder-Field.md)|Represents the generic builder object to which this non-generic instance delegates.|  
  
## See Also  
 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder?qualifyHint=False>   
 [Parallel Extension Internals for the .NET Framework](../Topic/Parallel%20Extension%20Internals%20for%20the%20.NET%20Framework.md)