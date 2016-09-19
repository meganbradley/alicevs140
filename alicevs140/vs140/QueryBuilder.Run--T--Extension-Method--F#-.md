---
title: "QueryBuilder.Run&lt;&#39;T&gt; Extension Method (F#)"
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
ms.assetid: d1f5e74f-fb0b-4c5d-9fa7-ba4dae215123
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QueryBuilder.Run&lt;&#39;T&gt; Extension Method (F#)
An extension method used to support the F# query syntax. Runs the given quotation as a query using LINQ IQueryable rules.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Run : Expr<QuerySource<'T,IQueryable>> -> IQueryable<'T>  
  
// Usage:  
queryBuilder.Run (quotation)  
```  
  
#### Parameters  
 `quotation`  
 Type: [Expr](../vs140/Quotations.Expr--T--Class--F#-.md)<[QuerySource](../vs140/Linq.QuerySource--T--Q--Class--F#-.md)<'T,                        <xref:System.Linq.IQueryable?qualifyHint=False>>>  
  
 A quotation expression tree that represents a query.  
  
## Return Value  
 The query as a queryable value.  
  
## Remarks  
 For more information and examples, see [Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md).  
  
## Platforms  
 Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2  
  
## Version Information  
 **F# Core Library Versions**  
  
 Supported in: 4.0Supported in: 4.0, Portable  
  
## See Also  
 [Linq.QueryBuilder Class (F#)](../Topic/Linq.QueryBuilder%20Class%20\(F%23\).md)   
 [Microsoft.FSharp.Linq Namespace (F#)](../vs140/Microsoft.FSharp.Linq-Namespace--F#-.md)   
 [Query Expressions (F#)](../Topic/Query%20Expressions%20\(F%23\).md)