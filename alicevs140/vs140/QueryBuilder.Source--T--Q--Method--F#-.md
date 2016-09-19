---
title: "QueryBuilder.Source&lt;&#39;T,&#39;Q&gt; Method (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
apilocation: 
  - FSharp.Core.dll
apitype: Assembly
ms.assetid: 5e0a1fed-f583-4d24-9921-765018ec926e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QueryBuilder.Source&lt;&#39;T,&#39;Q&gt; Method (F#)
A method used to support the F# query syntax. Inputs to queries are implicitly wrapped by a call to one of the overloads of this method.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Source : IQueryable<'T> -> QuerySource<'T,'Q>  
  
// Usage:  
queryBuilder.Source (source)  
```  
  
#### Parameters  
 `source`  
 Type: <xref:System.Linq.IQueryable`1?qualifyHint=False><'T>  
  
 The input queryable collection.  
  
## Return Value  
 A query in the form used by query expressions.  
  
## Remarks  
 For more information and examples, see [Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md).  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0, Portable  
  
## See Also  
 [Linq.QueryBuilder Class (F#)](../Topic/Linq.QueryBuilder%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)   
 [Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md)