---
title: "AsyncTaskMethodBuilder&lt;TResult&gt; Structure - Internal Members"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 17ebc340-8170-4aff-bf54-dc4548c83632
caps.latest.revision: 6
translation.priority.mt: 
  - de-de
  - ja-jp
---
# AsyncTaskMethodBuilder&lt;TResult&gt; Structure - Internal Members
This topic describes the internal members of the <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder`1?qualifyHint=False> class. For general information about this class, see the <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder`1?qualifyHint=False> reference topic.  
  
 **Namespace:** <xref:System.Runtime.CompilerServices?qualifyHint=True>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
 Because you cannot access these internal members from the .NET Framework, the following syntax is provided in Common Intermediate Language (CIL).  
  
## Syntax  
  
```  
.class public sequential ansi sealed beforefieldinit System.Runtime.CompilerServices.AsyncTaskMethodBuilder`1<TResult>  
       extends System.ValueType  
       implements System.Runtime.CompilerServices.IAsyncMethodBuilder  
```  
  
## Internal Members  
  
|Name|Description|  
|----------|-----------------|  
|[ObjectIdForDebugger property](../Topic/AsyncTaskMethodBuilder%3CTResult%3E.ObjectIdForDebugger%20Property.md)|Gets an object that may be used to uniquely identify this builder to the debugger.|  
|[m_task field](../vs140/AsyncTaskMethodBuilder-TResult-.m_task-Field.md)|Represents the lazily initialized built task.|  
  
## See Also  
 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder`1?qualifyHint=False>   
 [Parallel Extension Internals for the .NET Framework](../Topic/Parallel%20Extension%20Internals%20for%20the%20.NET%20Framework.md)