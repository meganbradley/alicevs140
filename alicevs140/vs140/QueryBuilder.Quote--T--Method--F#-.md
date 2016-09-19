---
title: "QueryBuilder.Quote&lt;&#39;T&gt; Method (F#)"
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
ms.assetid: 0e0e0a24-8646-41b7-93f0-7fdc13ed0875
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QueryBuilder.Quote&lt;&#39;T&gt; Method (F#)
A method used to support the F# query syntax. Indicates that the query should be passed as a quotation to the [Run](../Topic/QueryBuilder.Run%3C'T%3E%20Method%20\(F%23\).md) method.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Quote : Expr<'T> -> Expr<'T>  
  
// Usage:  
queryBuilder.Quote ()  
```  
  
#### Parameters  
 `source`  
 Type: [Expr](../vs140/Quotations.Expr--T--Class--F#-.md)<'T>  
  
 The input query.  
  
## Return Value  
 The query as an F# quotation.  
  
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