---
title: "QueryBuilder.ThenByDescending&lt;&#39;T,&#39;Q,&#39;Key&gt; Method (F#)"
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
ms.assetid: 75f16aa1-184b-4d6c-a880-0ce852e12a27
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QueryBuilder.ThenByDescending&lt;&#39;T,&#39;Q,&#39;Key&gt; Method (F#)
A query operator that performs a subsequent ordering of the elements selected so far in descending order by the given sorting key. This operator may only be used immediately after a `sortBy`, `sortByDescending`, `thenBy` or `thenByDescending`, or their nullable variants.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.ThenByDescending : QuerySource<'T,'Q> * ('T -> 'Key) -> QuerySource<'T,'Q> when 'Key : (IComparable)  
  
// Usage:  
queryBuilder.ThenByDescending (source, keySelector)  
```  
  
#### Parameters  
 `source`  
 Type: [QuerySource](../vs140/Linq.QuerySource--T--Q--Class--F#-.md)<'T,'Q>  
  
 The input query  
  
 `keySelector`  
 Type: 'T -> 'Key  
  
 Specifies the field to sort by.  
  
## Return Value  
 The sorted query.  
  
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