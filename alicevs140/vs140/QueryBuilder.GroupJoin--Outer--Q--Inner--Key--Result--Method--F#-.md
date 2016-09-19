---
title: "QueryBuilder.GroupJoin&lt;&#39;Outer,&#39;Q,&#39;Inner,&#39;Key,&#39;Result&gt; Method (F#)"
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
ms.assetid: a0a6c3b9-65fb-4bc6-bf05-c53ab4c6604f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QueryBuilder.GroupJoin&lt;&#39;Outer,&#39;Q,&#39;Inner,&#39;Key,&#39;Result&gt; Method (F#)
A query operator that correlates two sets of selected values based on matching keys and groups the results. Normal usage is `groupJoin (for y in elements2 -> key1 = key2) into group`.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.GroupJoin : QuerySource<'Outer,'Q> * QuerySource<'Inner,'Q> * ('Outer -> 'Key) * ('Inner -> 'Key) * ('Outer -> seq<'Inner> -> 'Result) -> QuerySource<'Result,'Q>  
  
// Usage:  
queryBuilder.GroupJoin (outerSource, innerSource, outerKeySelector, innerKeySelector, resultSelector)  
```  
  
#### Parameters  
 `outerSource`  
 Type: [QuerySource](../vs140/Linq.QuerySource--T--Q--Class--F#-.md)<'Outer,'Q>  
  
 The outer query.  
  
 `innerSource`  
 Type: [QuerySource](../vs140/Linq.QuerySource--T--Q--Class--F#-.md)<'Inner,'Q>  
  
 The inner query.  
  
 `outerKeySelector`  
 Type: 'Outer -> 'Key  
  
 A function that specifies the correlation key from the outer query.  
  
 `innerKeySelector`  
 Type: 'Inner -> 'Key  
  
 A function that specifies the correlation key from the inner query.  
  
 `resultSelector`  
 Type: 'Outer ->   [seq](../vs140/Collections.seq--T--Type-Abbreviation--F#-.md)<'Inner> ->   'Result  
  
 A function that returns the results of the operation.  
  
## Return Value  
 The resulting query.  
  
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