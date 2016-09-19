---
title: "LowPriority.RunQueryAsValue&lt;&#39;T&gt; Method (F#)"
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
ms.assetid: 152d4f48-b7da-4085-9ce3-44318aa8b9d6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LowPriority.RunQueryAsValue&lt;&#39;T&gt; Method (F#)
Runs a query to produce a simple value.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.RunQueryAsValue : Expr<'T> -> 'T  
  
// Usage:  
queryBuilder.RunQueryAsValue (expr)  
```  
  
#### Parameters  
 `expr`  
 Type: [Expr](../vs140/Quotations.Expr--T--Class--F#-.md)<'T>  
  
 The query as an expression.  
  
## Return Value  
 The query result as a simple value.  
  
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
 [QueryRunExtensions.LowPriority Module (F#)](../vs140/QueryRunExtensions.LowPriority-Module--F#-.md)