---
title: "QueryBuilder.Yield&lt;&#39;T,&#39;Q&gt; Method (F#)"
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
ms.assetid: 6634a987-e56a-486a-8d0a-b1d3218f16ff
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# QueryBuilder.Yield&lt;&#39;T,&#39;Q&gt; Method (F#)
A method used to support the F# query syntax. Returns a sequence of length one that contains the specified value.  
  
 **Namespace/Module Path**: Microsoft.FSharp.Linq  
  
 **Assembly**: FSharp.Core (in FSharp.Core.dll)  
  
## Syntax  
  
```  
// Signature:  
member this.Yield : 'T -> QuerySource<'T,'Q>  
  
// Usage:  
queryBuilder.Yield (value)  
```  
  
#### Parameters  
 `value`  
 Type: 'T  
  
 The value to wrap as a query.  
  
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